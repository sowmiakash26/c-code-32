#include<stdio.h>
void printarray(int arr[],int n){
    int i;
    for(i=0;i<n;i++){
        printf("%d", arr[i]);
}
}
int gcd(int a,int b){
    if(b==0)
        return 0;
    else
        return gcd(b,a%b);
}
void cycle(int arr[],int k, int n){
int i,j,a,temp;
k%=n;
int rotate =gcd(k,n);
for(i=0;i<n;i++){
    temp=arr[i];
    j=i;
    j=i;
    while(1){
        a=j+k;
        if(a>=n)
            a=a-n;
        if(a==i)
            break;
        arr[j]=arr[a];
        j=a;
    }
    arr[j]=temp;
}
}
int main()
{

    int arr[]={1,2,3,4,5};
    cycle(arr,2,5);
    printarray(arr,5);
    return 0;
