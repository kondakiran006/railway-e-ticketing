# railway-e-ticketing
namespace std;
class plat 
{ public: 
string tname,username,username1, password,tmppassword; 
int pno; 
int n,ip,i; 
int dif; 
string atime,dtime;
int tno; 
void authentification_details(); 
void login(); 
void get_traindetails();
void platform_controller();
};
void plat::authentification_details()
{ 
cout<<"\nEnter your username : ";
cin>>username; 
cout<<"\nEnter your password: ";
cin>>password; 
cout<<"\n--Registration Complete----\n 
cout<<"\n Press 1 to login ,2 to exit : "; 
cin>>ip; 
switch(ip) 
{ 
case 1: login(); 
break; 
default:
cout<<"\nexit\n"; 
} } 
void plat::login() 
{
cout<<"\n--login--------\n"; 
cout<<"\nEnter the username : ";
cin>>username1; 
cout<<"\nEnter the password : "; 
cin>>tmppassword; i=0; 
while(password[i]!='\0'||tmppassword[i]!='\0') 
{
dif=(password[i]-tmppassword[i]); 
if(dif!=0)
cout<<"\n Invalid username";
break;
i++;
}
if(dif==0) 
{
cout<<"\nLogin Successful";
} }
void plat::get_traindetails() 
{
int n=5;
cout<<"\n---Platform assignment system in train details---";
cout<<"\n1.A Train"; 
cout<<"\n--Platform -1 details----:";
cout<<"\nEnter the train-A ARRIVAL TIME:";
cin>>atime;
cout<<"Enter the Train-A DEPARTURE TIME:";
cin>>dtime; 
cout<<"\n2.B Train";
cout<<"\n---------Platform 2 details-----------:"; 
cout<<"\nEnter the train-B ARRIVAL TIME:";
cin>>atime;
cout<<"Enter the Train-B DEPARTURE TIME:";
cin>>dtime;
cout<<"\n3.C Train"; 
cout<<"\n--------Platform -3 details------------:";
cout<<"\nEnter the train-C ARRIVAL TIME:"; 
cin>>atime;
cout<<"Enter the Train-C DEPARTURE TIME:";
cin>>dtime;
cout<<"\n4.D Train";
cout<<"\n---------Platform 4 details-----------:";
cout<<"\nEnter the train-D ARRIVAL TIME:";
cin>>atime; 
cout<<"Enter the Train-D DEPARTURE TIME:";
cin>>dtime;
cout<<"\n5.E Train";
cout<<"\n----------Platform -5 details----------:";
cout<<"\nEnter the train-E ARRIVAL TIME:";
cin>>atime;
cout<<"Enter the Train-E DEPARTURE TIME:";
cin>>dtime;
cout<<"\nmaximum allocated platform is =\n"<<n;
}
void plat::platform_controller()
{
 cout<<"\nENTER THE NEW TRAIN NUMBER:";
 cin>>tno;
 cout<<"\n---check availability for platform-----";
 if(tno<=n)
 cout<<"\n Available for platform";
 else cout<<"\n PLATFORM ARE NOT AVAILABLE\n";
 }
 int main() 
 {
 int ch;
 plat p;
 p.authentification_details();
 do 
 {
 cout<<"\n1.Enter the train details"; 
 cout<<"\n2.Assign platform"; 
 cout<<"\nEnter the choice : ";
 cin>>ch; 
 switch(ch)
 { 
 case 1: p.get_traindetails();
 break; 
 case 2: p.platform_controller();
 break;
 default:
 cout<<"\n Enter the correct choice:\n"; 
 } }
 while(ch<=2); 
 }
