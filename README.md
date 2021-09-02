# MERGING-TWO-SORTED-ARRAYS
#include <iostream>

using namespace std;

int main()
{
    int m,n,i,j,k=0;
    cout<<"Enter the number of elements for array 1 \n";
    cin>>m;
    int a[m];
    cout<<"Enter "<<m<<" numbers in sorted manner \n";
    for(i=0;i<m;i++)
    cin>>a[i];
    
    cout<<"Enter the number of elements for array 2 \n";
    cin>>n;
    int b[n],c[m+n];
     cout<<"Enter "<<n<<" numbers in sorted manner \n";
    for(i=0;i<n;i++)
    cin>>b[i];
    
    i=0;
    j=0;
    while(i<m || j<n)
    {
        if(a[i]<b[j])
        {
            c[k++]=a[i++];
        }
        else
        {
            c[k++]=b[j++];
        }
    }
    
    cout<<"Merged Array : \n";
    for(i=0;i<m+n;i++)
    cout<<c[i]<<" ";

    return 0;
}
