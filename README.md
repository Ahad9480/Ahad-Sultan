#include<iostream>
#include<string>
#include<ctime>
#include<cstdlib>
#include<fstream>
using namespace std;
class portal {
 char name[100][100];
 char sub[10][10], c[10][10];
 int num,sbj,n_st,n_sbj,roll_num[30],total,percentage;
 double avg, g;
public:
 void getdata() {
 cout << "Enter the number of classes: ";
 cin >> num;
 for (int i = 0; i < num; i++) {
 cout << "Enter the name of class " << i + 1 << ": ";
 cin >> c[i];
 }
 for (int i = 0; i < num; i++) {
 cout << "Enter the number of students of class " << c[i] << ": ";
 cin >> sbj;
 cout << "Enter the details of students of class " << c[i] << endl;
 for (n_st = 0; n_st < sbj; n_st++) {
 cout << "Enter name of student " << n_st + 1 << ": ";
 cin >> name[n_st];
 cout << "Enter roll number of student " << n_st + 1 << ": ";
 cin >> roll_num[n_st];
 cout << "Enter the number of subjects of student " << n_st + 1 << ": ";
 cin >> n_sbj;
 cout << "Enter subjects of student " << n_st + 1 << ":" << endl;
 for (int k = 0; k < n_sbj; k++) {
 cin >> sub[k];
 }
 }
 }
 }
 void showdata() {
 for (int i = 0; i < num; i++) {
 cout << "Class " << c[i] << ":" << endl;
 for (n_st = 0; n_st < sbj; n_st++) {
 cout << "Name: " << name[n_st] << endl;
 cout << "Roll number: " << roll_num[n_st] << endl;
 cout << "Number of subjects: " << n_sbj << endl;
 cout << "Subjects: ";
 for (int k = 0; k < n_sbj; k++) {
 cout << sub[k] << " ";
 }
 cout << endl;
 }
 }
 }
 void calculate() {
 int wt;
 cout << "Enter weightage: ";
 cin >> wt;
 total = total + wt;
 avg = total / n_sbj;
 percentage = (avg / 100) * sbj;
 if (percentage >= 95) {
 g = 4;
 } else if (percentage >= 85 && percentage < 95) {
 g = 3.5;
 } else if (percentage >= 75 && percentage < 85) {
 g = 3.0;
 } else if (percentage >= 65 && percentage < 75) {
 g = 3;
 } else if (percentage >= 55 && percentage < 65) {
 g = 2.5;
 } else if (percentage >= 45 && percentage < 55) {
 g = 2.0;
 } else {
 g = 2;
 }
 cout << "GPA of the student is: " << g << endl;
 }
};
class Board {
public:
 char board[3][3];
 Board() {
 for (int i = 0; i < 3; i++) {
 for (int j = 0; j < 3; j++) {
 board[i][j] = '#';
 }
 }
 }
 void printBoard() {
 cout << "Current Board:" << endl;
 for (int i = 0; i < 3; i++) {
 for (int j = 0; j < 3; j++) {
 cout << board[i][j] << " ";
 }
 cout << endl;
 }
 cout << endl;
 }
 bool isFull() {
 for (int i = 0; i < 3; i++) {
 for (int j = 0; j < 3; j++) {
 if (board[i][j] == '#') {
 return false;
 }
 }
 }
 return true;
 }
};
class Game {
public:
 Board board;
 char currentPlayer;
 Game() {
 currentPlayer = 'X';
 }
 bool checkWin() {
 for (int i = 0; i < 3; i++) {
 if ((board.board[i][0] == currentPlayer && board.board[i][1] == currentPlayer && 
board.board[i][2] == currentPlayer) ||
 (board.board[0][i] == currentPlayer && board.board[1][i] == currentPlayer && 
board.board[2][i] == currentPlayer)) {
 return true;
 }
 }
 if ((board.board[0][0] == currentPlayer && board.board[1][1] == currentPlayer && 
board.board[2][2] == currentPlayer) ||
 (board.board[0][2] == currentPlayer && board.board[1][1] == currentPlayer && 
board.board[2][0] == currentPlayer)) {
 return true;
 }
 return false;
 }
 void playerTurn() {
 int row, col;
 while (true) {
 cout << "Player " << currentPlayer << ", enter row and column (0, 1, or 2) to place your mark: 
";
 cin >> row >> col;
 if (row < 0 || row > 2 || col < 0 || col > 2 || board.board[row][col] != '#') {
 cout << "Invalid move. Try again." << endl;
 continue;
 }
 board.board[row][col] = currentPlayer;
 break;
 }
 }
 void playGame() {
 while (true) {
 board.printBoard();
 playerTurn();
 if (checkWin()) {
 board.printBoard();
 cout << "Player " << currentPlayer << " wins!" << endl;
 break;
 }
 if (board.isFull()) {
 board.printBoard();
 cout << "It's a draw!" << endl;
 break;
 }
 currentPlayer = (currentPlayer == 'X') ? 'O' : 'X';
 }
 }
};
static int ch=50, wat=40, 
sam=30,roll=40,pizza=1000,d1=50,d2=80,d3=110,d4=150,b1=80,b2=150,b3=40,b4=200,b5=250,b6=1
80,f1=100,f2=150,c1=150,pulao=250,p2=150;
 
class menu
 {
 protected:
 string a;
 public:
 void mon()
 {
 cout<<"timmings 7am to 9 pm"<<endl;
 cout<<"chai(ch) RS."<<ch<<endl;
 cout<<"water(wat) RS."<<wat<<endl;
 cout<<"samosa(sam) RS."<<sam<<endl;
 cout<<"roll(roll) RS."<<roll<<endl;
 cout<<"drink RS."<<d1<<endl;
 cout<<" pizza "<<endl;
 cout<<"pizza RS."<<pizza<<endl;
 cout<<" biryani "<<endl;
 cout<<"biryani RS."<<b1<<endl;
 cout<<"biscuits(b3) RS."<<b3<<endl;
 cout<<" burger "<<endl;
 cout<<"burger RS."<<b4<<endl;
 }
 void tue()
 {
 cout<<"timmings 7am to 9 pm"<<endl;
 cout<<"chai(ch) RS."<<ch<<endl;
 cout<<"water(wat) RS."<<wat<<endl;
 cout<<"samosa(sam) RS."<<sam<<endl;
 cout<<"roll(roll) RS."<<roll<<endl;
 cout<<"drinks RS."<<d1<<endl;
 
 cout<<" pizza "<<endl;
 cout<<"pizza RS."<<pizza<<endl;
 cout<<" biryani "<<endl;
 cout<<"biryani RS."<<b1<<endl;
 cout<<"biscuits(b3) RS."<<b3<<endl;
 cout<<" fries "<<endl;
 cout<<" fries RS."<<f1<<endl;
 }
 void wed()
 {
 cout<<"timmings 7am to 9 pm"<<endl;
 cout<<"chai(ch) RS."<<ch<<endl;
 cout<<"water(wat) RS."<<wat<<endl;
 cout<<"samosa(sam) RS."<<sam<<endl;
 cout<<"roll(roll) RS."<<roll<<endl;
 cout<<"drinks RS."<<d1<<endl;
 cout<<" pizza "<<endl;
 cout<<"pizza RS."<<pizza<<endl;
 cout<<" pulao "<<endl;
 cout<<" pulao RS."<<pulao<<endl;
 cout<<" fries "<<endl;
 cout<<"fries RS."<<f1<<endl;
 }
 void thu()
 {
 cout<<"timmings 7am to 9 pm"<<endl;
 cout<<"chai(ch) RS."<<ch<<endl;
 cout<<"water(wat) RS."<<wat<<endl;
 cout<<"samosa(sam) RS."<<sam<<endl;
 cout<<"roll(roll) RS."<<roll<<endl;
 cout<<"drinks RS."<<d1<<endl;
 cout<<" biryani "<<endl;
 cout<<"biryani RS."<<b1<<endl;
 cout<<" burger "<<endl;
 cout<<"burger RS."<<b4<<endl;
 cout<<" fries "<<endl;
 cout<<"fries RS."<<f1<<endl;
 }
 void fri()
 {
 cout<<"timmings 7am to 9 pm"<<endl;
 cout<<"chai(ch) RS."<<ch<<endl;
 cout<<"water(wat) RS."<<wat<<endl;
 cout<<"samosa(sam) RS."<<sam<<endl;
 cout<<"roll(roll) RS."<<roll<<endl;
 cout<<"drinks RS."<<d1<<endl;
 cout<<" pizza "<<endl;
 cout<<"pizza RS."<<pizza<<endl;
 cout<<" biryani "<<endl;
 cout<<"biryani RS."<<b1<<endl;
 cout<<"biscuits(b3) RS."<<b3<<endl;
 cout<<" burger "<<endl;
 cout<<"burger RS."<<b4<<endl;
 }
 void sat()
 {
 cout<<"********closed****************"<<endl;
 
 }
 void sun()
 {
 cout<<"***********holiday***********"<<endl;
 
 }
 
};
 class entry
 {
 public:
 void mon_entry()
 {
 cout<<"for chai press 1 "<<endl;
 cout<<"for water press 2"<<endl;
 cout<<"for samosa press 3"<<endl;
 cout<<"for roll press 4"<<endl;
 cout<<"for drink press 5"<<endl;
 cout<<"for pizza press 6"<<endl;
 cout<<"for biryani press 7"<<endl;
 cout<<"for biscuit press 8"<<endl;
 }
 void tue_entry()
 {
 cout<<"for chai press 1 "<<endl;
 cout<<"for water press 2"<<endl;
 cout<<"for samosa press 3"<<endl;
 cout<<"for roll press 4"<<endl;
 cout<<"for drink press 5"<<endl;
 cout<<"for pizza press 6"<<endl;
 cout<<"for biryani press 7"<<endl;
 cout<<"for fries press 9"<<endl;
 
 }
 void wed_entry()
 {
 cout<<"for chai press 1 "<<endl;
 cout<<"for water press 2"<<endl;
 cout<<"for samosa press 3"<<endl;
 cout<<"for roll press 4"<<endl;
 cout<<"for drink press 5"<<endl;
 cout<<"for pizza press 6"<<endl;
 cout<<"for biscuit press 8"<<endl;
 cout<<"for pulao press 10"<<endl;
 }
 void thu_entry()
 {
 cout<<"for chai press 1 "<<endl;
 cout<<"for water press 2"<<endl;
 cout<<"for samosa press 3"<<endl;
 cout<<"for roll press 4"<<endl;
 cout<<"for drink press 5"<<endl;
 cout<<"for biryani press 7"<<endl;
 cout<<"for fries press 9"<<endl;
 cout<<"for burger press 11"<<endl;
 
 }
 void fri_entry()
 {
 cout<<"for chai press 1 "<<endl;
 cout<<"for water press 2"<<endl;
 cout<<"for samosa press 3"<<endl;
 cout<<"for roll press 4"<<endl;
 cout<<"for drink press 5"<<endl;
 cout<<"for pizza press 6"<<endl;
 cout<<"for biryani press 7"<<endl;
 cout<<"for burger press 11"<<endl;
 }
};
 class orders:public menu,public entry
 {
 public:
 int i,y[1],v[100],n[100],p1,p2,p3,p4,p5,p6,p7,p8,p9,p10,p11,price,x;
 int total;
 void mon_order()
 {
 p:
 cout<<"entry:"<<endl;
 cin>>v[i];
 switch(v[i])
 {
 case 1:
 cout<<"chai"<<endl;
 cout<<"no of chai:";
 cin>>n[0];
 p1=n[0]*ch;
 cout<<"price:"<<p1<<endl;
 break;
 case 2:
 cout<<"water "<<endl;
 cout<<"no of water bottle:";
 cin>>n[1];
 p2=n[1]*wat;
 cout<<"price:"<<p2<<endl;
 break;
 case 3:
 cout<<"samosa"<<endl;
 cout<<"no of samosa:";
 cin>>n[2];
 p3=n[2]*sam;
 cout<<"price:"<<p3<<endl;
 break;
 case 4:
 cout<<"roll "<<endl;
 cout<<"no of ROLL:";
 cin>>n[3];
 p4=n[3]*roll;
 cout<<"price:"<<p4<<endl;
 break;
 case 5:
 cout<<"drink"<<endl;
 cout<<"no of drink:";
 cin>>n[4];
 p5=n[4]*d1;
 cout<<"price:"<<p5<<endl;
 break;
 case 6:
 cout<<"pizza"<<endl;
 cout<<"no of pizza:";
 cin>>n[5];
 p6=n[5]*pizza;
 cout<<"price:"<<p6<<endl;
 break;
 case 7:
 cout<<"biryani "<<endl;
 cout<<"no of biryanis:";
 cin>>n[6];
 p7=n[6]*b1;
 cout<<"price:"<<p7<<endl;
 break;
 case 8:
 cout<<"biscuit"<<endl;
 cout<<"no of biscuit:";
 cin>>n[7];
 p8=n[7]*b3;
 cout<<"price:"<<p8<<endl;
 break;
 cout<<"invalid entry:"<<endl;
} 
 cout<<"press 1 for more items:"<<endl;
 cout<<"press other key for bill:";
 cin>>x;
 cout<<endl;
 if(x==1)
 {
 i++;
 goto p;
 }
 else
 {
 total=p1+p2+p3+p4+p5+p6+p7+p8+p9+p10+p11;
 cout<<"total price:"<<total<<endl;
}
}
 void tue_order()
 {
 p:
 cout<<"entry:"<<endl;
 cin>>v[i];
 switch(v[i])
 {
 case 1:
 cout<<"chai"<<endl;
 cout<<"no of chai:";
 cin>>n[0];
 p1=n[0]*ch;
 cout<<"price:"<<p1<<endl;
 break;
 case 2:
 cout<<"water "<<endl;
 cout<<"no of water bottle:";
 cin>>n[1];
 p2=n[1]*wat;
 cout<<"price:"<<p2<<endl;
 break;
 case 3:
 cout<<"samosa"<<endl;
 cout<<"no of samosa:";
 cin>>n[2];
 p3=n[2]*sam;
 cout<<"price:"<<p3<<endl;
 break;
 case 4:
 cout<<"roll "<<endl;
 cout<<"no of ROLL:";
 cin>>n[3];
 p4=n[3]*roll;
 cout<<"price:"<<p4<<endl;
 break;
 case 5:
 cout<<"drink"<<endl;
 cout<<"no of drink:";
 cin>>n[4];
 p5=n[4]*d1;
 cout<<"price:"<<p5<<endl;
 break;
 case 6:
 cout<<"pizza"<<endl;
 cout<<"no of pizza:";
 cin>>n[5];
 p6=n[5]*pizza;
 cout<<"price:"<<p6<<endl;
 break;
 case 7:
 cout<<"biryani "<<endl;
 cout<<"no of biryanis:";
 cin>>n[6];
 p7=n[6]*b1;
 cout<<"price:"<<p7<<endl;
 break;
 case 9:
 cout<<"fries"<<endl;
 cout<<"no of plates";
 cin>>n[7];
 p8=n[7]*f1;
 cout<<"price:"<<p8<<endl;
 break;
 cout<<"invalid entry:"<<endl;
} 
 cout<<"press 1 for more items:"<<endl;
 cout<<"press 0 for bill:";
 cin>>x;
 cout<<endl;
 if(x==1)
 {
 i++;
 goto p;
 }
 else if(x==0)
 {
 total=p1+p2+p3+p4+p5+p6+p7+p8+p9+p10+p11;
 cout<<"total price:"<<total<<endl;
}
}
 void wed_order()
 {
 p:
 cout<<"entry:"<<endl;
 cin>>v[i];
 switch(v[i])
 {
 case 1:
 cout<<"chai"<<endl;
 cout<<"no of chai:";
 cin>>n[0];
 p1=n[0]*ch;
 cout<<"price:"<<p1<<endl;
 break;
 case 2:
 cout<<"water "<<endl;
 cout<<"no of water bottle:";
 cin>>n[1];
 p2=n[1]*wat;
 cout<<"price:"<<p2<<endl;
 break;
 case 3:
 cout<<"samosa"<<endl;
 cout<<"no of samosa:";
 cin>>n[2];
 p3=n[2]*sam;
 cout<<"price:"<<p3<<endl;
 break;
 case 4:
 cout<<"roll "<<endl;
 cout<<"no of ROLL:";
 cin>>n[3];
 p4=n[3]*roll;
 cout<<"price:"<<p4<<endl;
 break;
 case 5:
 cout<<"drink"<<endl;
 cout<<"no of drink:";
 cin>>n[4];
 p5=n[4]*d1;
 cout<<"price:"<<p5<<endl;
 break;
 case 6:
 cout<<"pizza"<<endl;
 cout<<"no of pizza:";
 cin>>n[5];
 p6=n[5]*pizza;
 cout<<"price:"<<p6<<endl;
 break;
 case 8:
 cout<<"biscuit "<<endl;
 cout<<"no of biscuits:";
 cin>>n[6];
 p7=n[6]*b3;
 cout<<"price:"<<p7<<endl;
 break;
 case 10:
 cout<<"pulao"<<endl;
 cout<<"no of plates";
 cin>>n[7];
 p8=n[7]*pulao;
 cout<<"price:"<<p8<<endl;
 break;
 cout<<"invalid entry:"<<endl;
} 
 cout<<"press 1 for more items:"<<endl;
 cout<<"press 0 for bill:";
 cin>>x;
 cout<<endl;
 if(x==1)
 {
 i++;
 goto p;
 }
 else if(x==0)
 {
 total=p1+p2+p3+p4+p5+p6+p7+p8+p9+p10+p11;
 cout<<"total price:"<<total<<endl;
}
}
 void thu_order()
 {
 p:
 cout<<"entry:"<<endl;
 cin>>v[i];
 switch(v[i])
 {
 case 1:
 cout<<"chai"<<endl;
 cout<<"no of chai:";
 cin>>n[0];
 p1=n[0]*ch;
 cout<<"price:"<<p1<<endl;
 break;
 case 2:
 cout<<"water "<<endl;
 cout<<"no of water bottle:";
 cin>>n[1];
 p2=n[1]*wat;
 cout<<"price:"<<p2<<endl;
 break;
 case 3:
 cout<<"samosa"<<endl;
 cout<<"no of samosa:";
 cin>>n[2];
 p3=n[2]*sam;
 cout<<"price:"<<p3<<endl;
 break;
 case 4:
 cout<<"roll "<<endl;
 cout<<"no of ROLL:";
 cin>>n[3];
 p4=n[3]*roll;
 cout<<"price:"<<p4<<endl;
 break;
 case 5:
 cout<<"drink"<<endl;
 cout<<"no of drink:";
 cin>>n[4];
 p5=n[4]*d1;
 cout<<"price:"<<p5<<endl;
 break;
 case 7:
 cout<<"pizza"<<endl;
 cout<<"no of pizza:";
 cin>>n[5];
 p6=n[5]*pizza;
 cout<<"price:"<<p6<<endl;
 break;
 case 9:
 cout<<"fries "<<endl;
 cout<<"fries plates:";
 cin>>n[6];
 p7=n[6]*f1;
 cout<<"price:"<<p7<<endl;
 break;
 case 11:
 cout<<"burger"<<endl;
 cout<<"no of burgers";
 cin>>n[7];
 p8=n[7]*b2;
 cout<<"price:"<<p8<<endl;
 break;
 cout<<"invalid entry:"<<endl;
} 
 cout<<"press 1 for more items:"<<endl;
 cout<<"press 0 for bill:";
 cin>>x;
 cout<<endl;
 if(x==1)
 {
 i++;
 goto p;
 }
 else if(x==0)
 {
 total=p1+p2+p3+p4+p5+p6+p7+p8+p9+p10+p11;
 cout<<"total price:"<<total<<endl;
}
}
 void fri_order()
 {
 p:
 cout<<"entry:"<<endl;
 cin>>v[i];
 switch(v[i])
 {
 case 1:
 cout<<"chai"<<endl;
 cout<<"no of chai:";
 cin>>n[0];
 p1=n[0]*ch;
 cout<<"price:"<<p1<<endl;
 break;
 case 2:
 cout<<"water "<<endl;
 cout<<"no of water bottle:";
 cin>>n[1];
 p2=n[1]*wat;
 cout<<"price:"<<p2<<endl;
 break;
 case 3:
 cout<<"samosa"<<endl;
 cout<<"no of samosa:";
 cin>>n[2];
 p3=n[2]*sam;
 cout<<"price:"<<p3<<endl;
 break;
 case 4:
 cout<<"roll "<<endl;
 cout<<"no of ROLL:";
 cin>>n[3];
 p4=n[3]*roll;
 cout<<"price:"<<p4<<endl;
 break;
 case 5:
 cout<<"drink"<<endl;
 cout<<"no of drink:";
 cin>>n[4];
 p5=n[4]*d1;
 cout<<"price:"<<p5<<endl;
 break;
 case 6:
 cout<<"pizza"<<endl;
 cout<<"no of pizza:";
 cin>>n[5];
 p6=n[5]*pizza;
 cout<<"price:"<<p6<<endl;
 break;
 case 7:
 cout<<"biryani"<<endl;
 cout<<"no of plates of biryani:";
 cin>>n[6];
 p7=n[6]*b1;
 cout<<"price:"<<p7<<endl;
 break;
 case 11:
 cout<<"burger"<<endl;
 cout<<"no of burgers";
 cin>>n[7];
 p8=n[7]*b2;
 cout<<"price:"<<p8<<endl;
 break;
 cout<<"invalid entry:"<<endl;
} 
 cout<<"press 1 for more items:"<<endl;
 cout<<"press 0 for bill:";
 cin>>x;
 cout<<endl;
 if(x==1)
 {
 i++;
 goto p;
 }
 else if(x==0)
 {
 total=p1+p2+p3+p4+p5+p6+p7+p8+p9+p10+p11;
 cout<<"total price:"<<total<<endl;
}
}
};
class cancel:public orders
{
 public:
 int newprice,j,y[2],i,h[100],m[100],c1,c2,c3,c4,c5,c6,c7,c8,c9,c10,c11;
 void mon_cancel()
 {
 p:
 cout<<"enter the entry:";
 cin>>h[j];
 if(v[i]==h[j])
 {
 switch(v[j])
 {
 
 case 1:
 cout<<"chai"<<endl;
 cout<<"no of chai:";
 cin>>m[0];
if(m[0]<=n[0])
 {
 c1=m[0]*ch;
 cout<<"price:"<<c1<<endl;}
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
 break;
 case 2:
 cout<<"water "<<endl;
 cout<<"no of water bottle:";
 cin>>m[1];
 if(m[1]<=n[1])
{
 c2=m[1]*wat;
 cout<<"price:"<<c2<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
break;
 case 3:
 cout<<"samosa"<<endl;
 cout<<"no of samosa:";
 cin>>m[2];
 if(m[2]<=n[2]){
 c3=m[2]*sam;
 cout<<"price:"<<c3<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 4:
 cout<<"roll "<<endl;
 cout<<"no of ROLL:";
 cin>>m[3];
 if(m[3]<=n[3]){
 c4=m[3]*roll;
 cout<<"price:"<<c4<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 5:
 cout<<"drink"<<endl;
 cout<<"no of drink:";
 cin>>m[4];
 if(m[4]<=n[4])
{
c5=m[4]*d1;
 cout<<"price:"<<c5<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
 break;
 case 6:
 cout<<"pizza"<<endl;
 cout<<"no of pizza:";
 cin>>m[5];
 if(m[5]<=n[5])
 {
c6=m[5]*pizza;
 cout<<"price:"<<c6<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
break;
 case 7:
 cout<<"biryani "<<endl;
 cout<<"no of biryanis:";
 cin>>m[6];
 if(m[6]<=n[6]){
c7=m[6]*b1;
 cout<<"price:"<<c7<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 8:
 cout<<"biscuit"<<endl;
 cout<<"no of biscuit:";
 cin>>m[7];
 if(m[7]<=n[7])
 {
c8=m[7]*b3;
 cout<<"price:"<<c8<<endl;
 }
else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 cout<<"invalid entry:"<<endl;
 }
 cout<<"press 1 to cancel more items:"<<endl;
 cout<<"press 0 for bill:";
 cin>>x;
 cout<<endl;
 if(x==1)
 {
 i++;
 j++;
 goto p;
 }
 else if(x ==0)
 {
 newprice=(c1+c2+c3+c4+c5+c6+c7+c8+c9+c10+c11);
 cout<<"reduce price:"<<newprice<<endl;}
 }
 else 
 {
cout<<"wrong entry:"<<endl;
cout<<"select the item from buyed items:"<<endl;
goto p;
 }
 }
 void tue_cancel()
 {
 p:
 cout<<"enter the entry:";
 cin>>h[j];
 if(v[i]==h[j])
 {
 switch(v[j])
 {
 
 case 1:
 cout<<"chai"<<endl;
 cout<<"no of chai:";
 cin>>m[0];
if(m[0]<=n[0])
 {
 c1=m[0]*ch;
 cout<<"price:"<<c1<<endl;}
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
 break;
 case 2:
 cout<<"water "<<endl;
 cout<<"no of water bottle:";
 cin>>m[1];
 if(m[1]<=n[1])
{
 c2=m[1]*wat;
 cout<<"price:"<<c2<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
break;
 case 3:
 cout<<"samosa"<<endl;
 cout<<"no of samosa:";
 cin>>m[2];
 if(m[2]<=n[2]){
 c3=m[2]*sam;
 cout<<"price:"<<c3<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 4:
 cout<<"roll "<<endl;
 cout<<"no of ROLL:";
 cin>>m[3];
 if(m[3]<=n[3]){
 c4=m[3]*roll;
 cout<<"price:"<<c4<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 5:
 cout<<"drink"<<endl;
 cout<<"no of drink:";
 cin>>m[4];
 if(m[4]<=n[4])
{
c5=m[4]*d1;
 cout<<"price:"<<c5<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
 break;
 case 6:
 cout<<"pizza"<<endl;
 cout<<"no of pizza:";
 cin>>m[5];
 if(m[5]<=n[5])
 {
c6=m[5]*pizza;
 cout<<"price:"<<c6<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
break;
 case 7:
 cout<<"biryani "<<endl;
 cout<<"no of biryanis:";
 cin>>m[6];
 if(m[6]<=n[6]){
c7=m[6]*b1;
 cout<<"price:"<<c7<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 8:
 cout<<"fries"<<endl;
 cout<<"fries plates:";
 cin>>m[7];
 if(m[7]<=n[7])
 {
c8=m[7]*f1;
 cout<<"price:"<<c8<<endl;
 }
else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 cout<<"invalid entry:"<<endl;
 }
 cout<<"press 1 to cancel more items:"<<endl;
 cout<<"press 0 for bill:";
 cin>>x;
 cout<<endl;
 if(x==1)
 {
 i++;
 j++;
 goto p;
 }
 else if(x==0)
 {
 newprice=(c1+c2+c3+c4+c5+c6+c7+c8+c9+c10+c11);
 cout<<"reduce price:"<<newprice<<endl;}
 }
 else
 {
cout<<"wrong entry:"<<endl;
cout<<"select the item from buyed items:"<<endl;
goto p;
 }
 }
 void wed_cancel()
 {
 p:
 cout<<"enter the entry:";
 cin>>h[j];
 if(v[i]==h[j])
 {
 switch(v[j])
 {
 
 case 1:
 cout<<"chai"<<endl;
 cout<<"no of chai:";
 cin>>m[0];
if(m[0]<=n[0])
 {
 c1=m[0]*ch;
 cout<<"price:"<<c1<<endl;}
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
 break;
 case 2:
 cout<<"water "<<endl;
 cout<<"no of water bottle:";
 cin>>m[1];
 if(m[1]<=n[1])
{
 c2=m[1]*wat;
 cout<<"price:"<<c2<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
break;
 case 3:
 cout<<"samosa"<<endl;
 cout<<"no of samosa:";
 cin>>m[2];
 if(m[2]<=n[2]){
 c3=m[2]*sam;
 cout<<"price:"<<c3<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 4:
 cout<<"roll "<<endl;
 cout<<"no of ROLL:";
 cin>>m[3];
 if(m[3]<=n[3]){
 c4=m[3]*roll;
 cout<<"price:"<<c4<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 5:
 cout<<"drink"<<endl;
 cout<<"no of drink:";
 cin>>m[4];
 if(m[4]<=n[4])
{
c5=m[4]*d1;
 cout<<"price:"<<c5<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
 break;
 case 6:
 cout<<"pizza"<<endl;
 cout<<"no of pizza:";
 cin>>m[5];
 if(m[5]<=n[5])
 {
c6=m[5]*pizza;
 cout<<"price:"<<c6<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
break;
 case 8:
 cout<<"biscuits "<<endl;
 cout<<"no of biscuits:";
 cin>>m[6];
 if(m[6]<=n[6]){
c7=m[6]*b3;
 cout<<"price:"<<c7<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 10:
 cout<<"pulao"<<endl;
 cout<<"pulao plates:";
 cin>>m[7];
 if(m[7]<=n[7])
 {
c8=m[7]*p1;
 cout<<"price:"<<c8<<endl;
 }
else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 cout<<"invalid entry:"<<endl;
 }
 cout<<"press 1 to cancel more items:"<<endl;
 cout<<"press 0 for bill:";
 cin>>x;
 cout<<endl;
 if(x==1)
 {
 i++;
 j++;
 goto p;
 }
 else if(x==0)
 {
 newprice=(c1+c2+c3+c4+c5+c6+c7+c8+c9+c10+c11);
 cout<<"reduce price:"<<newprice<<endl;}
 }
 else
 {
cout<<"wrong entry:"<<endl;
cout<<"select the item from buyed items:"<<endl;
goto p;
 }
 }
 void thu_cancel()
 {
 p:
 cout<<"enter the entry:";
 cin>>h[j];
 if(v[i]==h[j])
 {
 switch(v[j])
 {
 
 case 1:
 cout<<"chai"<<endl;
 cout<<"no of chai:";
 cin>>m[0];
if(m[0]<=n[0])
 {
 c1=m[0]*ch;
 cout<<"price:"<<c1<<endl;}
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
 break;
 case 2:
 cout<<"water "<<endl;
 cout<<"no of water bottle:";
 cin>>m[1];
 if(m[1]<=n[1])
{
 c2=m[1]*wat;
 cout<<"price:"<<c2<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
break;
 case 3:
 cout<<"samosa"<<endl;
 cout<<"no of samosa:";
 cin>>m[2];
 if(m[2]<=n[2]){
 c3=m[2]*sam;
 cout<<"price:"<<c3<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 4:
 cout<<"roll "<<endl;
 cout<<"no of ROLL:";
 cin>>m[3];
 if(m[3]<=n[3]){
 c4=m[3]*roll;
 cout<<"price:"<<c4<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 5:
 cout<<"drink"<<endl;
 cout<<"no of drink:";
 cin>>m[4];
 if(m[4]<=n[4])
{
c5=m[4]*d1;
 cout<<"price:"<<c5<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
 break;
 case 7:
 cout<<"pizza"<<endl;
 cout<<"no of pizza:";
 cin>>m[5];
 if(m[5]<=n[5])
 {
c6=m[5]*pizza;
 cout<<"price:"<<c6<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
break;
 case 9:
 cout<<"fries "<<endl;
 cout<<"no of plates:";
 cin>>m[6];
 if(m[6]<=n[6]){
c7=m[6]*f1;
 cout<<"price:"<<c7<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 11:
 cout<<"burger"<<endl;
 cout<<"no of burger:";
 cin>>m[7];
 if(m[7]<=n[7])
 {
c8=m[7]*b2;
 cout<<"price:"<<c8<<endl;
 }
else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 cout<<"invalid entry:"<<endl;
 }
 cout<<"press 1 to cancel more items:"<<endl;
 cout<<"press 0 for bill:";
 cin>>x;
 cout<<endl;
 if(x==1)
 {
 i++;
 j++;
 goto p;
 }
 else if(x==0)
 {
 newprice=(c1+c2+c3+c4+c5+c6+c7+c8+c9+c10+c11);
 cout<<"reduce price:"<<newprice<<endl;}
 }
 else
 {
cout<<"wrong entry:"<<endl;
cout<<"select the item from buyed items:"<<endl;
goto p;
 }
 }
 void fri_cancel()
 {
 p:
 cout<<"enter the entry:";
 cin>>h[j];
 if(v[i]==h[j])
 {
 switch(v[j])
 {
 
 case 1:
 cout<<"chai"<<endl;
 cout<<"no of chai:";
 cin>>m[0];
if(m[0]<=n[0])
 {
 c1=m[0]*ch;
 cout<<"price:"<<c1<<endl;}
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
 break;
 case 2:
 cout<<"water "<<endl;
 cout<<"no of water bottle:";
 cin>>m[1];
 if(m[1]<=n[1])
{
 c2=m[1]*wat;
 cout<<"price:"<<c2<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
break;
 case 3:
 cout<<"samosa"<<endl;
 cout<<"no of samosa:";
 cin>>m[2];
 if(m[2]<=n[2]){
 c3=m[2]*sam;
 cout<<"price:"<<c3<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 4:
 cout<<"roll "<<endl;
 cout<<"no of ROLL:";
 cin>>m[3];
 if(m[3]<=n[3]){
 c4=m[3]*roll;
 cout<<"price:"<<c4<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 5:
 cout<<"drink"<<endl;
 cout<<"no of drink:";
 cin>>m[4];
 if(m[4]<=n[4])
{
c5=m[4]*d1;
 cout<<"price:"<<c5<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
 break;
 case 6:
 cout<<"pizza"<<endl;
 cout<<"no of pizza:";
 cin>>m[5];
 if(m[5]<=n[5])
 {
c6=m[5]*pizza;
 cout<<"price:"<<c6<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
}
break;
 case 7:
 cout<<"biryani "<<endl;
 cout<<"no of plates :";
 cin>>m[6];
 if(m[6]<=n[6]){
c7=m[6]*b1;
 cout<<"price:"<<c7<<endl;
 }
 else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 case 11:
 cout<<"burger"<<endl;
 cout<<"no of burger:";
 cin>>m[7];
 if(m[7]<=n[7])
 {
c8=m[7]*b2;
 cout<<"price:"<<c8<<endl;
 }
else
 {
 cout<<"invalid:"<<endl;
 goto p;
 }
break;
 cout<<"invalid entry:"<<endl;
 }
 cout<<"press 1 to cancel more items:"<<endl;
 cout<<"press 0 for bill:";
 cin>>x;
 cout<<endl;
 if(x==1)
 {
 i++;
 j++;
 goto p;
 }
 else if(x==0)
 {
 newprice=(c1+c2+c3+c4+c5+c6+c7+c8+c9+c10+c11);
 cout<<"reduce price:"<<newprice<<endl;}
 }
 else
 {
cout<<"wrong entry:"<<endl;
cout<<"select the item from buyed items:"<<endl;
goto p;
 }
 }
}; 
int main() {
 int choice;
 while (true) 
{
cout<<"===========Welcome to Air 
University Managment System=========="<<endl;
 cout<<"Select an option"<<endl;
 cout<< "1. Teacher Portal\n";
 cout<< "2. University Cafe\n";
 cout<< "3. Gaming Zone\n";
 cout<<"4. Exit\n";
 cout<<"Enter your choice: ";
 cin>>choice;
 switch (choice) {
 case 1: {
 portal teacherPortal;
 teacherPortal.getdata();
 teacherPortal.showdata();
 teacherPortal.calculate();
 break;
 }
 case 2: {
 orders cafeOrders;
 int cafeChoice;
 while (true) {
 cout << "\nUniversity Cafe Menu:\n";
 cout << "1. Monday Menu\n";
 cout << "2. Tuesday Menu\n";
 cout << "3. Wednesday Menu\n";
 cout << "4. Thursday Menu\n";
 cout << "5. Friday Menu\n";
 cout << "6. Saturday Menu\n";
 cout << "7. Cancel Order\n";
 cout << "8. Exit Cafe\n";
 cout << "Enter your choice: ";
 cin >> cafeChoice;
 switch (cafeChoice) {
 case 1:
 cafeOrders.mon_order();
 break;
 case 2:
 cafeOrders.tue_order();
 break;
 case 3:
 cafeOrders.wed_order();
 break;
 case 4:
 cafeOrders.thu_order();
 break;
 case 5:
 cafeOrders.fri_order();
 break;
 
 
 case 6: {
 cancel cancelOrder;
 int cancelChoice;
 cout << "Select day to cancel order:\n";
 cout << "1. Monday\n2. Tuesday\n3. Wednesday\n4. Thursday\n5. Friday\n";
 cin >> cancelChoice;
 switch (cancelChoice) {
 case 1:
 cancelOrder.mon_cancel();
 break;
 case 2:
 cancelOrder.tue_cancel();
 break;
 case 3:
 cancelOrder.wed_cancel();
 break;
 case 4:
 cancelOrder.thu_cancel();
 break;
 case 5:
 cancelOrder.fri_cancel();
 break;
 default:
 cout << "Invalid choice." << endl;
 }
 break;
 }
 case 8:
 cout << "Exiting Cafe." << endl;
 break;
 default:
 cout << "Invalid choice. Try again." << endl;
 }
 if (cafeChoice == 8) 
{
 break; 
 }
 }
 break;
 }
 case 3: {
 Game game;
 game.playGame();
 break;
 }
 case 4:
 cout << "Exiting program. Goodbye!" << endl;
 return 0;
 default:
 cout << "Invalid choice. Try again." << endl;
 }
 }
}
