# Design Graphics - Paithan Office App (Python Console Version)

clients = []
projects = [
    {"name": "Shubham Reels", "status": "Editing"},
    {"name": "Grocery Logo", "status": "In Design"},
    {"name": "Marriage Card", "status": "Final Touch"}
]

def show_menu():
    print("\n===== Design Graphics - Paithan Office =====")
    print("1. Add New Client")
    print("2. View Clients")
    print("3. View Ongoing Projects")
    print("4. Contact / Booking Info")
    print("5. Exit")

def add_client():
    name = input("Enter Client Name: ")
    service = input("Service Type (Logo / Poster / Reels / Edit): ")
    phone = input("Contact Number: ")
    clients.append({"name": name, "service": service, "phone": phone})
    print(f"✅ Client '{name}' added successfully!")

def view_clients():
    if not clients:
        print("⚠️ No clients added yet.")
    else:
        print("\n--- Registered Clients ---")
        for idx, client in enumerate(clients, 1):
            print(f"{idx}. {client['name']} - {client['service']} - {client['phone']}")

def view_projects():
    print("\n--- Ongoing Projects ---")
    for idx, proj in enumerate(projects, 1):
        print(f"{idx}. {proj['name']} - {proj['status']}")

def contact_info():
    print("\n📞 Contact: +91 98765 43210")
    print("📍 Location: Paithan, Aurangabad")
    print("📲 WhatsApp: https://wa.me/919876543210")

# Main App Loop
while True:
    show_menu()
    choice = input("Choose an option (1-5): ")

    if choice == "1":
        add_client()
    elif choice == "2":
        view_clients()
    elif choice == "3":
        view_projects()
    elif choice == "4":
        contact_info()
    elif choice == "5":
        print("👋 Exiting... Thank you!")
        break
    else:
        print("❌ Invalid choice. Try again.")
