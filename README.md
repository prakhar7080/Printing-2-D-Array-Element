# Printing-2-D-Array-Element
#include<iostream>
using namespace std;
void row_wise_printing(int a[][3],int rownumber, int colnumber){
    for(int i=0;i<rownumber;i++){
        for(int j=0;j<colnumber;j++){
            cout<<a[i][j]<<" ";
        }
        cout<<endl;
    }
}
void col_wise_printing(int a[][3],int rownumber, int colnumber){
    for(int j=0;j<rownumber;j++){
        for(int i=0;i<colnumber;i++){
            cout<<a[i][j]<<" ";
        }
        cout<<endl;
    }
}
void first_diagonal_printing(int a[][3],int rownumber,int colnumber){
    for(int i=0;i<rownumber;i++){
        for(int j=0;j<colnumber;j++){
            if(i==j) cout<<a[i][j]<<" ";
        }
    }
}
void second_diagonal_printing(int a[][3],int rownumber,int colnumber){
    for(int i=0;i<rownumber;i++){
        for(int j=0;j<colnumber;j++){
            if(i+j == rownumber-1) cout<<a[i][j]<<" ";
        }
    }
}
int main(){
    int a[3][3] = {
                    {1,2,3},
                    {4,5,6},
                    {7,8,9}
                };
    int rownumber = 3;
    int colnumber = 3;
    // row_wise_printing(a,rownumber,colnumber);
    // col_wise_printing(a,rownumber,colnumber);
    // first_diagonal_printing(a,rownumber,colnumber);
    second_diagonal_printing(a,rownumber,colnumber);
    return 0;
}
