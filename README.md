# Introduction-to-computers
Computer is an electronic device that processes data according to instructions provided by software programs. It takes input (data), processes it using a central processing unit (CPU), stores information, and produces output (results) to perform various tasks. It is widely used in fields such as education, business, communication, and entertainment for efficient and accurate operations

## Types Of Computers
Computers are amazing electronic devices that help us learn, play, work, and connect with the world. They store information, process data, and produce results based on our instructions. With artificial intelligence (AI), some computers can even learn from data! Computers come in different types based on their size and data-handling capabilities. This guide explains these types in a way that’s easy to understand, with examples relevant to students.
- Super Computer
- MainFrame Computers
- MiniComputers
- Personal Computers
- Embedded Computers

## History Of Computers
The history of computers began in the 1800s when Charles Babbage designed the Analytical Engine, an early concept for a programmable computer. In the 1940s, the first electronic computers, such as ENIAC, were developed. During the 1950s and 1960s, transistors and integrated circuits made computers smaller, faster, and more reliable. In the 1970s, the invention of the microprocessor led to the development of personal computers. During the 1980s and 1990s, computers became common in homes, schools, and offices, while the invention of the World Wide Web expanded their usefulness. Today, computers are found in smartphones, laptops, cars, and many other devices, and technologies such as cloud computing and artificial intelligence continue to make them more powerful and useful.
[History Of Computer](https://en.wikipedia.org/wiki/Computer)

## Example Code
tasks = []

def show_tasks():
    if not tasks:
        print("\nYour to-do list is empty.")
    else:
        print("\nYour Tasks:")
        for i, task in enumerate(tasks, 1):
            print(f"{i}. {task}")

def add_task():
    task = input("Enter a new task: ")
    tasks.append(task)
    print("Task added successfully!")

def remove_task():
    show_tasks()

    if tasks:
        try:
            number = int(input("Enter the task number to remove: "))
            removed = tasks.pop(number - 1)
            print(f"Removed: {removed}")
        except (ValueError, IndexError):
            print("Invalid task number.")

while True:
    print("\n--- TO-DO LIST ---")
    print("1. Show tasks")
    print("2. Add task")
    print("3. Remove task")
    print("4. Exit")

    choice = input("Choose an option: ")

    if choice == "1":
        show_tasks()
    elif choice == "2":
        add_task()
    elif choice == "3":
        remove_task()
    elif choice == "4":
        print("Goodbye!")
        break
    else:
        print("Invalid choice. Please try again.")
