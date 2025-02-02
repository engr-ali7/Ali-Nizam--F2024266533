//The comments in the project are defining the functionality or certain elements alongside the sections of code and their programmers.
#include <iostream>
#include <string>
#include<iomanip>
#include"Section.h"
using namespace std;
//prices for the default products in the product menu:
int prices[10] = { 239000, 319000, 519000, 579000, 369000, 409000, 469000, 589000,120000,220000 };
//default stock quantities for products shown in menu:
int available_stock[10] = { 20,20,10,5,20,15,15,2,20,30 };
//constant variable for number of max items that can be included.
const int MAX_ITEMS = 10;
//size of the array was set to max items to ensure no extra laptops can be added
string laptops[MAX_ITEMS];
int laptopCount = 0;
void ratings();
void addLaptop();

void displayLaptops() {
    if (laptopCount == 0) {
        cout << "thats all." << endl;
        return;
    }
    for (int i = 0; i < laptopCount; ++i) 
	{
        cout<< "|" << laptops[i] << endl;
    }
}

bool stock_check(int order_amount,int order_number) 
{
    if (available_stock[order_number-1]>=order_amount)
    {
        return true ;
    }
    else
    {
        return false ;
    }
}
float price_calculation(int order_amount,int order_price) 
{
    double discout = 0.0 ;
    int total_price = order_amount*order_price;
    if (order_amount==2)
    {
        discout = 0.05 ;
    }
    else if (order_amount>2&&order_amount<5)
    {
        discout = 0.075;
    }
    else if (order_amount>=5)
    {
        discout = 0.1;
    }
    total_price = total_price * 1.16;
    total_price = total_price - total_price * discout;
    return total_price;
}

int main()
{	ammar:
	
    bool main_exit=true;
    while(main_exit)
    {
    int login_type,password_work;
    string password="ALPHAbeta",enter_password;
    bool pass=false;
    for(;;)
    {
    if(pass==false)
    {

    cout<<"Choose login type\n"<<"1 - Admin login(Password protected)\n"<<"2 - User login(No password)\n";
    cin>>login_type;
    if(login_type==1)
    {
        password_work=1;
        for(;;)
        {
            if (password_work==1)
                {
                cout<<"Enter password\n";
                cin>>enter_password;
                    if(enter_password==password)
                    {
                        pass=true;
                        cout<<"\n\nYou have entered as admin.\n";
                        cin.ignore();
                        break;
                    }
                    else
                    {
                    cout<<"Wrong password. Try again\n";
                    cout<<"Press 1 to Try Again.\n";
                    cout<<"Press 0 to Choose login type\n";
                    cin>>password_work;
                    }
                }
                else
                {
                    break;
                }
        }
    }
    else if(login_type==2)
    {
        cout<<"You have entered as user.\n";
        cin.ignore();
        break;
    }
    }
    else
    {
        break;
    }
    }
	//User Interface 
    if(!pass)
    {
    cout << " ______________________________________________________________________________________________________\n";
    cout << "|   MACBOOK MODEL     |  GPU   |   CPU   | RAM  | STORAGE | PRODUCT CODE |     PRICE| AVAILAIBLE STOCK |\n";
    cout << "| 11-INCH MACBOOK AIR | M1 PRO | 16-CORE | 16GB | 256GB   |      0       |   "<<prices[0]<<"  |               "<<available_stock[0]<<" |\n";
    cout << "| 16-INCH MACBOOK AIR | M1 PRO | 16-CORE | 32GB | 512GB   |      1       |   "<<prices[1]<<"  |               "<<available_stock[1]<<" |\n";
    cout << "| 16-INCH MACBOOK AIR | M1 MAX | 24-CORE | 32GB | 1TB     |      2       |   "<<prices[2]<<"  |               "<<available_stock[2]<<" |\n";
    cout << "| 11-INCH MACBOOK PRO | M1 MAX | 24-CORE | 64GB | 8TB     |      3       |   "<<prices[3]<<"  |                "<<available_stock[3]<<" |\n";
    cout << "| 11-INCH MACBOOK PRO | M1 MAX | 32-CORE | 64GB | 1TB     |      4       |   "<<prices[4]<<"  |               "<<available_stock[4]<<" |\n";
    cout << "| 16-INCH MACBOOK PRO | M2     | 32-CORE | 64GB | 2TB     |      5       |   "<<prices[5]<<"  |               "<<available_stock[5]<<" |\n";
    cout << "| 16-INCH MACBOOK PRO | M1 PRO | 32-CORE | 64GB | 4TB     |      6       |   "<<prices[6]<<"  |               "<<available_stock[6]<<" |\n";
    cout << "| 16-INCH MACBOOK PRO | M2 MAX | 32-CORE | 64GB | 8TB     |      7       |   "<<prices[7]<<"  |                "<<available_stock[7]<<" |\n";
    cout << "|";displayLaptops();cout<<"                                         8      |   "<<prices[8]<<"  |                "<<available_stock[8]<<" |\n";
    cout << "|";displayLaptops();cout<<"		                                 9       |   "<<prices[9]<<"  |                "<<available_stock[9]<<" |\n";
    cout << "|____________________|________|_________|______|_________|________________|___________|__________________|\n";

    int bought_stock[8] = { 0,0,0,0,0,0,0,0 };
    int order_number, ORDER_amount, santa , confirm, payment_method, CONTINUATION, in_total_price, total_price, type_of_orders;
    CONTINUATION = 1;
    string aloo_shora ;
    in_total_price = 0;
    bool availability;
    string address, name;
    for (int i = 0;; i++)
    {	//how many times the use interface runs.
        cout << "HOW MANY TYPES OF LAPTOPS DO YOU NEED TO PURCHASE = ";
        cin >> type_of_orders;
        for (int b = 0; b < type_of_orders; b++)
        {
            cout << "\n\n\nENTER THE PRODUCT CODE OF THE LAPTOP YOU WANT TO PURCHASE = ";
            cin >> order_number;
            cout << "\nHOW MANY LAPTOPS DO YOU NEED = ";
            cin >> ORDER_amount;
            availability = stock_check(ORDER_amount, order_number);
            if (availability)
            {
                cout << "\n\n\nTHE AMOUNT REQUIRED IS AVAILABLE.\nPRESS 1 TO CONFIRM YOUR ORDER = \n";
                cin >> confirm;
                if (confirm == 1)
                {
                    total_price = price_calculation(ORDER_amount, prices[order_number - 1]);
                    in_total_price = total_price + in_total_price;
                    bought_stock[order_number - 1] = bought_stock[order_number - 1] + ORDER_amount;
                }
                else
                {
                    cout << "PRESS 1 TO CONTINUE AND 0 TO EXIT = '\n";
                }
            }
            else
            {
                cout << "THE REQUIRED AMOUNT IS NOT AVAILABLE...PRESS 1 TO CONTINUE SHOPPING 1 AND O TO EXIT.";
                cin >> CONTINUATION;
            }
            if (CONTINUATION != 1)
            {
                break;
                availability = true;
            }
            availability = true;
        }
            if (availability)
            {	//aloo shora ignores input buffers desi jugar for input buffer logical err.
                getline(cin, aloo_shora);
                cout << "\nENTER DELIVERY ADDRESS = ";
                getline( cin , address );
                cout << "CONFIRM DELIVERY ADDRESS = " << address << "\nPRESS 1 TO CONFIRM = \n";
                cin >> santa;
                cout << "\nENTER RECIPIENT NAME = ";
                getline(cin, aloo_shora); 
                getline( cin , name);
                cout << "YOUR TOTAL BILL IS = " << in_total_price << endl ;
                cout << " _____________________________\n";
                cout << "|CASH ON DELIVERY       |   1 |\n";
                cout << "|CARD ON DELIVERY       |   2 |\n";
                cout << "|EASYPAISA ON DELIVERY  |   3 |\n";
                cout << "|PAYMENT METHOD         |   4 |\n";
                cout << "|_______________________|_____|\n";
                cin >> payment_method;
                cout << "\n\nCONFIRM ORDER BY PRESSING 1 \n";
                cin >> confirm;
                if (confirm == 1)
                {
                    available_stock[order_number - 1] = available_stock[order_number - 1] - ORDER_amount;
                    cout << "THANK'S FOR THE SHOPPING!\n";
                    cout<<"Order was delivered to your doorstep:"<<endl;
                    ratings();
                    cout<<endl;
                    for (int l = 0; l < 8; l++)
                    {
                        available_stock[l] = available_stock[l] - bought_stock[l];
                    }
                }
                cout << "PRESS 1 TO CONTINUE SHOPPING AND 0 TO END SHOPPING.\n";
                cin >> CONTINUATION;
            }
            else
            {
                cout << "YOUR DESIRED PRODUCT IS NOT AVAILABLE. \nPRESS 1 TO CONTINUE SHOPPING AND 0 TO END SHOPPING.\n";
                cin >> CONTINUATION;
            }
            if (CONTINUATION != 1)
            {
                break;
            }
            cout<<"DO YOU WANT TO EXIT THE APP\n0 - YES\n1 - NO\n";
            cin>>main_exit;
            return 0;
}
 
}
if(pass)
{
    for(;;)
    {
    int admin_num,change_type,new_price,new_quant;
    bool loop_1=false,exit;
    cout << " _____________________________________________________________________________________________________\n";
    cout << "|   MACBOOK MODEL     |  GPU   |   CPU   | RAM  | STORAGE | PRODUCT CODE | PRICE   | AVAILAIBLE STOCK |\n";
    cout << "| 11-INCH MACBOOK AIR | M1 PRO | 16-CORE | 16GB | 256GB   |      0       | "<<prices[0]<<"  |               "<<available_stock[0]<<" |\n";
    cout << "| 16-INCH MACBOOK AIR | M1 PRO | 16-CORE | 32GB | 512GB   |      1       | "<<prices[1]<<"  |               "<<available_stock[1]<<" |\n";
    cout << "| 16-INCH MACBOOK AIR | M1 MAX | 24-CORE | 32GB | 1TB     |      2       | "<<prices[2]<<"  |               "<<available_stock[2]<<" |\n";
    cout << "| 11-INCH MACBOOK PRO | M1 MAX | 24-CORE | 64GB | 8TB     |      3       | "<<prices[3]<<"  |                "<<available_stock[3]<<" |\n";
    cout << "| 11-INCH MACBOOK PRO | M1 MAX | 32-CORE | 64GB | 1TB     |      4       | "<<prices[4]<<"  |               "<<available_stock[4]<<" |\n";
    cout << "| 16-INCH MACBOOK PRO | M2     | 32-CORE | 64GB | 2TB     |      5       | "<<prices[5]<<"  |               "<<available_stock[5]<<" |\n";
    cout << "| 16-INCH MACBOOK PRO | M1 PRO | 32-CORE | 64GB | 4TB     |      6       | "<<prices[6]<<"  |               "<<available_stock[6]<<" |\n";
    cout << "| 16-INCH MACBOOK PRO | M2 MAX | 32-CORE | 64GB | 8TB     |      7       | "<<prices[7]<<"  |                "<<available_stock[7]<<" |\n";
    cout << "|                     |        |         |      |         |              |                  |               |\n";
    cout << "|_____________________|________|_________|______|_________|______________|__________________|__________________|\n";
	int c;
	cout<<"Enter 1 to add a new item to the software or 2 for standard admin choices and 3 to exit "<<endl;
	cin>>c;
	switch(c)
	{
	
		case 1: addLaptop();
		break;
	case 2:{
		
	
	for(;;)
    {
    cout<<endl<<endl<<"ENTER THE CODE OF PRODUCT YOU WANT TO CHANGE"<<endl;
    cin>>admin_num;
    if(admin_num>=0 && admin_num<=8)
    {
    cout<<"YOU WANT TO CHANGE:\n1 - PRICE\n2 - QUANTITY\n";
    cin>>change_type;
    if(change_type==1 || change_type==2)
    {
        loop_1=true;
        break;
    }
    else
    {
        cout<<"Please enter correct number for price or quantity\n";
    }
    }
    else
    {
        cout<<"ENTER CORRECT CODE\n";
    }


    }
    if(loop_1)
    {
        if(change_type==1)
        {
            cout<<"What do you want the price to be?\n";
            cin>>new_price;
            prices[admin_num-1]=new_price;
            for(;;)
            {
            cout<<"What do you want the price to be?\n";
            cin>>new_price;
            if(new_price>0)
            {
                prices[admin_num]=new_price;
                break;
            }
            else
            {
                cout<<"ENTER A NON-ZERO AMOUNT\n";
            }
            }
        }
        if(change_type==2)
        {
            for(;;)
            {
            cout<<"What number of items would you like to add\n ";
            cin>>new_quant;
            if(new_quant>0)
            {
                available_stock[admin_num]=available_stock[admin_num]+new_quant;
                break;
            }
            else
            {
                cout<<"ENTER A NON-ZERO AMOUNT\n";
            }
            }
        
        }
    }
    cout<<"Press 1 to continue changing and 0 to exit\n";
    cin>>exit;
    if(!exit)
    {
        break;
    }
    else
    {
        continue;
        break;
    }
    break;
    case 3:  goto ammar;
	default: cout<<"invalid input";
	}

    cout<<"DO YOU WANT TO EXIT THE APP\n1 - YES\n0 - NO\n";

    cin>>main_exit;
  
}
}
}
}
return 0;
}
void addLaptop() {
    if (laptopCount >= MAX_ITEMS) {
        cout << "Store is full. Cannot add more laptops." << endl;
        return;
    }

    string name, price, cpu, gpu, quantity;
     // ignores the input buffer ie. \n.
	cin.ignore();
    cout << "Enter laptop name: ";
    getline(cin, name);
    cout << "Enter CPU details: ";
    getline(cin, cpu);
    cout << "Enter GPU details: ";
    getline(cin, gpu);
    

    // Combine all specifications into a single string
    //the + joins the "name" with the input of name and so on.
    laptops[laptopCount] = "|\t " + name +
                           "|\t" + cpu + 
                           "|\t" + gpu;
    laptopCount++;
    cout << "Laptop added successfully!" << endl;
}

