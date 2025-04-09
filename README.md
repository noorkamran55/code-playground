#include <iostream>
using namespace std;

int main() {
    const int REGULAR_RATE = 300;
    const int OVERTIME_RATE = 400;
    const int REGULAR_HOURS = 40;

    float hoursWorked, pay, totalSalary = 0;

    for (int i = 1; i <= 10; i++) {
        cout << "Enter hours worked by employee " << i << ": ";
        cin >> hoursWorked;

        if (hoursWorked <= REGULAR_HOURS) {
            pay = hoursWorked * REGULAR_RATE;
        } else {
            float overtimeHours = hoursWorked - REGULAR_HOURS;
            pay = (REGULAR_HOURS * REGULAR_RATE) + (overtimeHours * OVERTIME_RATE);
        }

        cout << "Weekly pay for employee " << i << ": Rs. " << pay << endl;
        totalSalary += pay;
    }

    cout << "\nTotal salary to be paid to all 10 employees: Rs. " << totalSalary << endl;
//totalsalary=totalsalary+pay;
    return 0;
}
