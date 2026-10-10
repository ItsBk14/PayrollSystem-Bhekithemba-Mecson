#include <iostream>

using namespace std;

int main()
{
    // Author: Bhekithemba Mecson - Gauteng City College
    int numEmployees;
    int empId;
    string empName;
    double basicSalary;
    string department;
    int rating;
    int years;

    cout << "=== Gauteng City College Payroll System ===" << endl;
    cout << "How many employees to process? ";
    cin >> numEmployees;

    // Validation for number of employees
    if (numEmployees <= 0) {
        cout << "Error: Number of employees must be greater than 0!" << endl;
        return 0;
    }

    // For loop - repeats for known number of employees
    for (int i = 1; i <= numEmployees; i++) {
        cout << "\n--- Employee " << i << " ---" << endl;
        cout << "Enter Employee ID (int): ";
        cin >> empId;

        cout << "Enter Employee Name: ";
        cin.ignore(); // clear buffer
        getline(cin, empName);

        cout << "Enter Basic Salary (double): ";
        cin >> basicSalary;

        // Error handling for negative salary
        if (basicSalary < 0) {
            cout << "Error: Salary cannot be negative! Skipping this employee." << endl;
            continue;
        }

        cout << "Enter Department (IT / Sales / HR): ";
        cin >> department;

        cout << "Enter Performance Rating (1-5): ";
        cin >> rating;

        cout << "Enter Years of Service: ";
        cin >> years;

        double perfBonus = 0;
        double deptBonus = 0;
        double loyaltyBonus = 0;

        // if-else for performance bonus - my rule choice
        if (rating == 5) {
            perfBonus = basicSalary * 0.25; // 25% for excellent
        } else if (rating == 4) {
            perfBonus = basicSalary * 0.15; // 15% for good
        } else if (rating == 3) {
            perfBonus = basicSalary * 0.05; // 5% for average
        } else {
            perfBonus = 0;
        }

        // switch for department bonus - my rule choice
        // Using first letter for switch: I=IT, S=Sales, H=HR
        char deptCode = department[0];
        switch (deptCode) {
            case 'I':
            case 'i':
                deptBonus = 1000; // IT brings system support
                break;
            case 'S':
            case 's':
                deptBonus = 2000; // My custom rule: Sales brings money so R2000
                break;
            case 'H':
            case 'h':
                deptBonus = 500; // HR
                break;
            default:
                deptBonus = 0;
                break;
        }

        // Loyalty bonus
        if (years > 5) {
            loyaltyBonus = basicSalary * 0.05; // extra 5% for loyalty >5 years
        }

        double totalBonus = perfBonus + deptBonus + loyaltyBonus;
        double totalPay = basicSalary + totalBonus;

        // Payslip output
        cout << "\n===== PAYSLIP =====" << endl;
        cout << "Employee: " << empName << " (ID: " << empId << ")" << endl;
        cout << "Department: " << department << endl;
        cout << "Basic Salary: R" << basicSalary << endl;
        cout << "Performance Bonus: R" << perfBonus << endl;
        cout << "Department Bonus: R" << deptBonus << endl;
        cout << "Loyalty Bonus: R" << loyaltyBonus << endl;
        cout << "Total Bonus: R" << totalBonus << endl;
        cout << "Total Pay: R" << totalPay << endl;
        cout << "===================" << endl;
    }

    cout << "\nPayroll processing complete. Thank you!" << endl;
    return 0;
}
