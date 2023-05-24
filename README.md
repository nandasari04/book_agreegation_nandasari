# book_agreegation_nandasari
class Book:
    def __init__(self, title, author, price):
        self.title = title
        self.author = author
        self.price = price

    def __str__(self):
        return f"{self.title} by {self.author} - ${self.price:.2f}"


class Bookstore:
    def __init__(self, name):
        self.name = name
        self.books = []

    def add_book(self, book):
        self.books.append(book)

    def display_books(self):
        print(f"Buku tersedia di {self.name}:")
        if self.books:
            for book in self.books:
                print(book)
        else:
            print("buku tidak tersedia.")


# Contoh penggunaan program
book1 = Book("Python Programming", "John Smith", 29.99)
book2 = Book("Java Basics", "Jane Doe", 24.99)
book3 = Book("C++ Fundamentals", "Alice Johnson", 19.99)

bookstore = Bookstore("MyBookstore")
bookstore.add_book(book1)
bookstore.add_book(book2)
bookstore.add_book(book3)

bookstore.display_books()
