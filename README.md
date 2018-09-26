# StructExc5
Informatics Coursebook, Structure, p143

// Да се напише програма, която създава структура Firma с полета name, egn, duty и payment, указващи името на работник във фирмата, неговото ЕГН, длъжност и заплата. Да се въведе цяло число n и след него n на брой данни от тип Firma. Да се изведат имената на тези работници, чиято заплата е по-малка от 700 лв

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
