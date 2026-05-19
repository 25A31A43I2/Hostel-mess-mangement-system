#include <iostream>
using namespace std;

class HostelMess {
private:
    int studentId;
    string studentName;
    int breakfast;
    int lunch;
    int dinner;
    float totalBill;

public:
    void input() {
        cout << "Enter Student ID: ";
        cin >> studentId;

        cout << "Enter Student Name: ";
        cin >> studentName;

        cout << "Enter Number of Breakfasts Taken: ";
        cin >> breakfast;

        cout << "Enter Number of Lunches Taken: ";
        cin >> lunch;

        cout << "Enter Number of Dinners Taken: ";
        cin >> dinner;

        calculateBill();
    }

    void calculateBill() {
        totalBill = (breakfast * 30) + (lunch * 50) + (dinner * 60);
    }

    void display() {
        cout << "\n========== MESS BILL DETAILS ==========\n";
        cout << "Student ID       : " << studentId << endl;
        cout << "Student Name     : " << studentName << endl;
        cout << "Breakfast Count  : " << breakfast << endl;
        cout << "Lunch Count      : " << lunch << endl;
        cout << "Dinner Count     : " << dinner << endl;
        cout << "Total Mess Bill  : Rs. " << totalBill << endl;
    }
};

int main() {
    HostelMess student;

    cout << "========================================\n";
    cout << "   HOSTEL MESS MANAGEMENT SYSTEM\n";
    cout << "========================================\n";

    student.input();

    student.display();

    cout << "\nThank You for Using the System!\n";

    return 0;
}
