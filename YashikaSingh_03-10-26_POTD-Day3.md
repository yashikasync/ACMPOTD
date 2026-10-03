# POTD
## EXPLANATION
First, we take all the elements as input and store them in a vector. We then sort the vector in increasing order so that the smallest elements come first. 
After sorting, we check the elements starting from the second position and compare each one with the minimum element. If we find an element strictly greater than the 
minimum, it is the required second order statistic, so we print it and stop. If no such element exists, it means all the elements are equal, so we print "NO".
## CODE
#include <bits/stdc++.h>
using namespace std;
int main() {
    int n,i;
    cin>>n;
    vector <int>a(n);
    for(i=0;i<n;i++){
        cin>>a[i];
    }
    sort(a.begin(),a.end());
    for(i=1;i<n;i++){
        if(a[i]>a[0]){
            cout<<a[i];
            return 0;
        }
    }
    cout<<"NO";
    return 0;
}
<img width="1920" height="1080" alt="Screenshot (662)" src="https://github.com/user-attachments/assets/12b5716e-0b0f-480d-9c4e-7e38d6c1b1cf" />
