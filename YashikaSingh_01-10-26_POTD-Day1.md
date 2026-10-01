# POTD Day 1
## Solution Explanation

First, we traverse the entire grid and find the positions of all `*` characters.
We maintain four variables:
`minRow` – smallest row containing `*`
`maxRow` – largest row containing `*`
`minCol` – smallest column containing `*`
`maxCol` – largest column containing `*`
Whenever we find a `*`, we update these four boundaries.
After traversing the complete grid, these boundaries represent the smallest rectangle containing all the `*` characters.
Finally, we print all the elements between `minRow` and `maxRow` and between `minCol` and `maxCol`.

## Code
#include <bits/stdc++.h>
using namespace std;
int main() {
    int n,m;
    cin>>n>>m;
    vector <string>a(n);
    int minRow=n,maxRow=-1;
    int minCol=m,maxCol=-1;
    for(int i=0;i<n;i++){
        cin>>a[i];
        for(int j=0;j<m;j++){
            if(a[i][j]=='*'){
                minRow=min(minRow,i);
                maxRow=max(maxRow,i);
                minCol=min(minCol,j);
                maxCol=max(maxCol,j);
            }
        }
    }
    for(int i=minRow;i<=maxRow;i++){
        for(int j=minCol;j<=maxCol;j++){
            cout<<a[i][j];
        }
        cout<<'\n';
    }
    return 0;
}
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/eef371ce-24aa-4ab3-8df9-1410ae55ba00" />
