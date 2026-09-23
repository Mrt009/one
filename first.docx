#include <iostream>
#include <string>
using namespace std;

class BedAllocation
{
private:
    string patientName;
    string wardType;
    int days;
    int totalCharge;

public:

    // Default constructor
    BedAllocation()
    {
        patientName = "";
        wardType = "";
        days = 0;
        totalCharge = 0;
    }

    // Constructor for General Ward
    // Rs. 500 per day
    BedAllocation(string name, int d)
    {
        patientName = name;
        wardType = "General Ward";
        days = d;
        totalCharge = 500 * days;
    }

    // Constructor for Semi-Private Ward
    // Rs. 1500 per day
    BedAllocation(string name, int d, char)
    {
        patientName = name;
        wardType = "Semi-Private";
        days = d;
        totalCharge = 1500 * days;
    }

    // Constructor for Private Room
    // Rs. 3000 per day
    BedAllocation(string name, int d, float)
    {
        patientName = name;
        wardType = "Private Room";
        days = d;
        totalCharge = 3000 * days;
    }

    // Constructor for ICU
    // Rs. 8000 per day + Rs. 2000 fixed charge
    BedAllocation(string name, int d, bool)
    {
        patientName = name;
        wardType = "ICU";
        days = d;
        totalCharge = (8000 * days) + 2000;
    }

    // Display patient details
    void display()
    {
        cout << "Patient Name : " << patientName << endl;
        cout << "Ward Type    : " << wardType << endl;
        cout << "Days         : " << days << endl;
        cout << "Total Charge : Rs. " << totalCharge << endl;
        cout << "-----------------------------" << endl;
    }
};

int main()
{
    // Creating four patient objects using constructor overloading
    BedAllocation p1("Rahul", 3);
    BedAllocation p2("Amit", 4, 'S');
    BedAllocation p3("Priya", 2, 1.0f);
    BedAllocation p4("Neha", 3, true);

    // Array of objects to store four patients
    BedAllocation patients[4];

    patients[0] = p1;
    patients[1] = p2;
    patients[2] = p3;
    patients[3] = p4;

    // Display all patient records
    cout << "HOSPITAL BED ALLOCATION DETAILS" << endl;
    cout << "================================" << endl;

    for (int i = 0; i < 4; i++)
    {
        patients[i].display();
    }

    return 0;
}

========================================================================================

#include <iostream>
using namespace std;

class Product
{
private:
    int price;

public:

    // Constructor
    Product(int p)
    {
        price = p;
    }

    // Overload + operator
    Product operator+(Product p)
    {
        Product temp(0);
        temp.price = price + p.price;
        return temp;
    }

    // Overload > operator
    bool operator>(Product p)
    {
        return price > p.price;
    }

    // Overload == operator
    bool operator==(Product p)
    {
        return price == p.price;
    }

    // Display price
    void display()
    {
        cout << price << endl;
    }
};

int main()
{
    Product p1(1000), p2(500), p4(1000);

    // Add prices of p1 and p2
    Product p3 = p1 + p2;

    cout << "Sum of prices: ";
    p3.display();

    // Compare p1 and p2
    if (p1 > p2)
    {
        cout << "Product 1 is costlier" << endl;
    }

    // Compare p1 and p4
    if (p1 == p4)
    {
        cout << "Product 1 and Product 4 have the same price" << endl;
    }

    return 0;
}
