#include <iostream>
#include <string>
using namespace std;

int main() {
    const int MAX = 100;
    int id[MAX];
    string name[MAX];
    string course[MAX];
    float prelim[MAX], midterm[MAX], finals[MAX], average[MAX];
    string remarks[MAX];
    int count = 0;
    int choice;

    do {
        cout << "\n===== STUDENT LIST AND GRADING SYSTEM =====\n";
        cout << "1. Add Student\n";
        cout << "2. View Students\n";
        cout << "3. Search Student\n";
        cout << "4. Delete Student\n";
        cout << "5. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;
        cin.ignore();

        if (choice == 1) {
            if (count < MAX) {
                cout << "\nEnter Student ID: ";
                cin >> id[count];
                cin.ignore();
                cout << "Enter Name: ";
                getline(cin, name[count]);
                cout << "Enter Course: ";
                getline(cin, course[count]);

                cout << "Enter Prelim Grade: ";
                cin >> prelim[count];
                cout << "Enter Midterm Grade: ";
                cin >> midterm[count];
                cout << "Enter Final Grade: ";
                cin >> finals[count];

                
                average[count] = (prelim[count] * 0.3) + (midterm[count] * 0.3) + (finals[count] * 0.4);

                if (average[count] >= 75)
                    remarks[count] = "Passed";
                else
                    remarks[count] = "Failed";

                count++;
                cout << "\nStudent record added successfully!\n";
            } else {
                cout << "\nMaximum number of students reached!\n";
            }
        }

        else if (choice == 2) {
            if (count == 0) {
                cout << "\nNo student records found.\n";
            } else {
                cout << "\n--- STUDENT LIST ---\n";
                for (int i = 0; i < count; i++) {
                    cout << "\nStudent ID: " << id[i];
                    cout << "\nName: " << name[i];
                    cout << "\nCourse: " << course[i];
                    cout << "\nPrelim: " << prelim[i];
                    cout << "\nMidterm: " << midterm[i];
                    cout << "\nFinals: " << finals[i];
                    cout << "\nAverage: " << average[i];
                    cout << "\nRemarks: " << remarks[i] << "\n";
                }
            }
        }

        else if (choice == 3) {
            int searchID;
            bool found = false;
            cout << "\nEnter ID to search: ";
            cin >> searchID;

            for (int i = 0; i < count; i++) {
                if (id[i] == searchID) {
                    cout << "\n--- STUDENT FOUND ---\n";
                    cout << "Name: " << name[i] << endl;
                    cout << "Course: " << course[i] << endl;
                    cout << "Prelim: " << prelim[i] << endl;
                    cout << "Midterm: " << midterm[i] << endl;
                    cout << "Finals: " << finals[i] << endl;
                    cout << "Average: " << average[i] << endl;
                    cout << "Remarks: " << remarks[i] << endl;
                    found = true;
                }
            }

            if (!found)
                cout << "\nNo student found with that ID.\n";
        }

        else if (choice == 4) {
            int deleteID;
            bool deleted = false;
            cout << "\nEnter ID to delete: ";
            cin >> deleteID;

            for (int i = 0; i < count; i++) {
                if (id[i] == deleteID) {
                    for (int j = i; j < count - 1; j++) {
                        id[j] = id[j + 1];
                        name[j] = name[j + 1];
                        course[j] = course[j + 1];
                        prelim[j] = prelim[j + 1];
                        midterm[j] = midterm[j + 1];
                        finals[j] = finals[j + 1];
                        average[j] = average[j + 1];
                        remarks[j] = remarks[j + 1];
                    }
                    count--;
                    cout << "\nStudent record deleted successfully!\n";
                    deleted = true;
                    break;
                }
            }

            if (!deleted)
                cout << "\nNo student found with that ID.\n";
        }

        else if (choice == 5) {
            cout << "\nExiting program... Goodbye!\n";
        }

        else {
            cout << "\nInvalid choice. Please try again.\n";
        }

    } while (choice != 5);

    return 0;
}
