# POTD DAY 2
## EXPLANATION
First, we store the entire flag in a vector of strings.
For every row, we check whether all characters in that row are the same as the first character of that row. If any character is different, the row is invalid, so we print `NO`.
Then, we check every pair of consecutive rows. We compare the first character of the current row with the first character of the previous row. If they are the same, two adjacent rows have the same color, so we print `NO`.
If all rows contain the same color and every pair of consecutive rows has different colors, the flag is valid, so we print `YES`.
## CODE
#include <bits/stdc++.h>
using namespace std;
int main(){
    int n,m;
    cin>>n>>m;
    vector<string>a(n);
    for(int i=0;i<n;i++) cin>>a[i];
    for(int i=0;i<n;i++){
        for(int j=1;j<m;j++){
            if(a[i][j]!=a[i][0]){
                cout<<"NO";
                return 0;
            }
        }
    }
    for(int i=1;i<n;i++){
        if(i>0 && a[i][0]==a[i-1][0]){
            cout<<"NO";
            return 0;
        }
    }
    cout<<"YES";
    return 0;
}
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a95ce3dd-d126-4a31-be63-e8d0ed2b03ea" />
