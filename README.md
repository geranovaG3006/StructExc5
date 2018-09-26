# StructExc5
Informatics Coursebook, Structure, p143

#include<iostream>
using namespace std;
struct Firma
{
  char name[20];
  char egn[20];
  char duty[40];
  double payment;
};
int main()
{
	Firma employees[100];
	int n;
	cout<<"Br employees=";
	cin>>n;
	for(int i=0;i<n;i++)
	{
		cout<<"Name=";
		cin.get();
        cin.getline(employees[i].name,40);
		cout<<"EGN=";
		cin>>employees[i].egn;
		cout<<"Duty=";
		cin>>employees[i].duty;
		cout<<"Payment=";
		cin>>employees[i].payment;
	}
    cout<<"Payment below 700:"<<endl;
	for(int i=0;i<n;i++)
	{
		if(employees[i].payment<700) 
		{
		cout<<employees[i].name<<endl;
		}
	}
	system("pause");
	return 0;
}
