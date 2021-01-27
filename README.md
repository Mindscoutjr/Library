#include <iostream>
  
#include <string.h>

using namespace std;


class books

{

    char author,title,publisher;
    
    int price;
    
    static int count;
    
    public:
    
        books(void); 
        
        void display_stock(void);
        
        void search(void);
        
};

int books :: count=0;

books :: books(void)
{

  author = newchar[15];
  
  title = newchar[15];
  
  publisher = newchar[15];
  
  price = newint[15];
  
    for(int i=0;i<15;i++)
    
        {
        
            author[i] = newchar;
            
            title[i] = newchar;
            
            publisher[i] = newchar;
            
       }
       
}


void books :: getdata(void)

{
  cout<<"\nEnter Book name:";
  
  cin>>title[count];
  
  cout<<"Enter Author name:";
  
  cin>>author[count];
  
  cout<<"Enter Publisher of book:";
  
  cin>>publisher[count];
  
  cout<<"Enter Price of book:";
  
  cin>>price[count];
  
  count++;
  
  
}

void books :: display_stock(void)

{



cout<<"\n\n\n";

cout<<"Book Name"<<setw(15)<<"Author Name"<<setw(20)<<"Publisher"<<setw(10)<<"Price"<<endl;

for(int i=0;i<count;i++)

{

cout<<setw(15)<<title[i]<<setw(20)<<author[i]<<setw(20)<<publisher[i]<<setw(10)<<price[i]<<endl;

}

cout<<"\n\nTotal Number of Books are "<<count;

}


void books :: search(void)

{



 char  name[20],writer[20];
 
 cout<<"\n\n\nEnter Book name:";
 
 cin>>name;
 
 cout<<"Enter Author of Book:";
 
 cin>>writer;
 
 for(int i=0;i<count;i++)
 
 {
 
   if((title[i],name)==0) && ((author[i],writer)==0))
   
     {
     
     cout<<"\n\nEntered Information Book Available\n";
     
     cout<<"Price of that book is "<<price[i];
     
     }
     
 }
 
 cout<<"\n\nBook is not Available in stock\n";
 
}


void main()

{
    
    books o1;
    
    int choice;
    
    while(1)
    
    cout<<"\n\nChoose your choice\n";
    
    cout<<"1) Enter Information for  your book\n";
    
    cout<<"2) To See stock\n";
    
    cout<<"3) To Search for a Particular book\n";
    
    cout<<"4) Exit\n";
    
    cout<<"Enter your choice:";
    
    cin>>choice;
    
    switch(choice)
    {
    
    case 1 : o1.getdata();
    
    break;
    
    case 2 : o1.display_stock();
    
    break;
    
    case 3 : o1.search();
    
    break;
    
    case 4 : break;
    
cout<<"\n\nEnter choice is invalid\nTry again\n";

 }
 
}

