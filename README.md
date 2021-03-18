#include<iostream>

using namespace std;
 
void permute(string& str, int l, int r)
{
 
   
    if (l == r) {
        if (str.find("AB") == string::npos)
            cout << str << " ";
        return;
    }
 
    for (int i = l; i <= r; i++) {
        swap(str[l], str[i]);
        permute(str, l + 1, r);
        swap(str[l], str[i]);
    }
}
int main()
{
    string str = "ABC";
    permute(str, 0, str.length() - 1);
    return 0;
}
