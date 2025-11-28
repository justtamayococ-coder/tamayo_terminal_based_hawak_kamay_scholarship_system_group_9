# tamayo_terminal_based_hawak_kamay_scholarship_system_group_9
description
# Terminal-Based Hawak Kamay Scholarship Monitoring System
# Sample code snippet

scholars = []

def add_scholar():
    name = input("Enter Student Name: ")
    sid = input("Enter Student ID: ")
    course = input("Enter Course: ")
    year = input("Enter Year Level: ")
    status = input("Enter Scholarship Status (Active/Renewed/Graduated/Terminated): ")

    scholar = {
        "Name": name,
        "ID": sid,
        "Course": course,
        "Year": year,
        "Status": status
    }
    scholars.append(scholar)
    print("\nScholar record added successfully!\n")

def view_scholars():
    if not scholars:
        print("No scholar records found.\n")
    else:
        print("\nList of Hawak Kamay Scholars:")
        for s in scholars:
            print(f"{s['ID']} - {s['Name']} ({s['Course']} - {s['Status']})")

def main():
    while True:
        print("\n=== Hawak Kamay Scholarship Monitoring System ===")
        print("[1] Add Scholar")
        print("[2] View Scholars")
        print("[3] Exit")
        choice = input("Select an option: ")

        if choice == "1":
            add_scholar()
        elif choice == "2":
            view_scholars()
        elif choice == "3":
            print("Exiting system... Goodbye!")
            break
        else:
            print("Invalid choice. Please try again.\n")

main()
