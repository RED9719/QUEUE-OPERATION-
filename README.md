# QUEUE-OPERATION-
queue = list()

def enqueue(item):
    queue.append(item)
    print("Item added to the queue")

def dequeue():
    if len(queue) == 0:
        print("Queue is empty")
    else:
        item_1 = int(input("Enter the item to delete: "))
        queue.pop(item_1)
        print("Element removed from the queue")


def display():
    if len(queue) == 0:
        print("Queue is empty!")
    else:
        print(queue)

def menu():
    while True:
        print("Queue Operations Menu:")
        print("1. Enqueue")
        print("2. Dequeue")
        print("3. Display")
        print("4. Exit")
        ch = input("Enter your choice: ")

        if ch == '1':
            item = input("Enter the item to enqueue: ")
            enqueue(item)
        elif ch == '2':
            dequeue()
        elif ch == '3':
            display()
        elif ch == '4':
            print("Exiting program")
            break
        else:
            print("Invalid choice.")

menu()
