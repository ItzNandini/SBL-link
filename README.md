```SBL
Here are the algorithms for each of your Python programs, broken down into logical steps.

## **1. Swapping & Number Check**
 1. **Start**
 2. **Input:** Accept two numbers, num1 and num2.
 3. **Process (Swap):**
   * Store the value of num1 in a temporary variable (temp).
   * Assign the value of num2 to num1.
   * Assign the value of temp to num2.
 4. **Output:** Display the swapped values of num1 and num2.
 5. **Decision:** * If num1 > 0, output "Positive".
   * Else if num1 < 0, output "Negative".
   * Else, output "Zero".
 6. **Stop**

## **2. Simple Calculator**
 1. **Start**
 2. **Display:** Show the menu of operations (1. Add, 2. Sub, 3. Mul, 4. Div).
 3. **Input:** Accept two numbers and an operation choice (1–4).
 4. **Decision (Operations):**
   * If choice is 1: Calculate num1 + num2.
   * If choice is 2: Calculate num1 - num2.
   * If choice is 3: Calculate num1 * num2.
   * If choice is 4:
     * Check if num2 is not zero. If true, calculate num1 / num2.
     * If num2 is zero, output an error message.
 5. **Output:** Display the result of the calculation.
 6. **Stop**

## **3. Factorial & Fibonacci (Recursion)**
**Factorial Algorithm:**
 1. **Define Function:** If n is 0 or 1, return 1 (**Base Case**).
 2. Otherwise, return n * factorial(n - 1) (**Recursive Step**).
 3. **Input:** Accept a number and call the function.
**Fibonacci Algorithm:**
 1. **Define Function:** * If n is 0, return 0.
   * If n is 1, return 1.
   * Otherwise, return fib(n-1) + fib(n-2).
 2. **Loop:** Iterate from 0 to the desired number of terms and call the function for each index.

## **4. GUI with Tkinter**
 1. **Start**
 2. **Initialize:** Create the main application window and set dimensions.
 3. **Create Widgets:** Add a label (instruction), an entry box (input), and a button (action).
 4. **Define Event:** Create a function that:
   * Retrieves text from the entry box.
   * Updates a display label with a "Hello" greeting.
 5. **Main Loop:** Run the application to keep the window open and listen for button clicks.
 6. **Stop**

## **5. Exception Handling**
 1. **Start**
 2. **Try Block:**
   * Input two integers.
   * Attempt to divide the first by the second.
 3. **Except Block:**
   * If the user enters text instead of numbers, catch ValueError.
   * If the second number is zero, catch ZeroDivisionError.
 4. **Else Block:** If no errors occur, display the division result.
 5. **Finally Block:** Always print "Program execution completed."
 6. **Stop**

## **6. NLTK (NLP Processing)**
 1. **Start**
 2. **Setup:** Download necessary NLTK datasets (punkt, wordnet).
 3. **Tokenization:** Break the input sentence into individual words/tokens.
 4. **Stemming:** Strip suffixes from words to get the root form (e.g., "learning" becomes "learn").
 5. **Lemmatization:** Convert words to their dictionary base form using context.
 6. **Sentiment Analysis:** Use the VADER tool to calculate positive, negative, and neutral scores.
 7. **Output:** Display the tokens, stems, lemmas, and sentiment scores.
 8. **Stop**

## **7. Web Scraper (BeautifulSoup & Selenium)**
**BeautifulSoup (Static):**
 1. **Request:** Send an HTTP GET request to the URL.
 2. **Parse:** Convert the raw HTML into a searchable "soup" object.
 3. **Extract:** Find the <title> tag and print its text.
**Selenium (Dynamic):**
 1. **Initialize:** Open a web browser via a driver (e.g., Chrome).
 2. **Navigate:** Go to the specific URL and wait for the page to load.
 3. **Locate:** Find an element (e.g., h1) using the DOM structure.
 4. **Close:** Print the element text and shut down the browser.

## **8. Packet Sniffing (Scapy)**
 1. **Start**
 2. **Define Callback:** Create a function to process every captured packet.
 3. **Filter:** Within the function, check if the packet has an **IP layer**.
 4. **Extract:** Read the Source IP and Destination IP from the packet header.
 5. **Sniff:** Start the capture process for a specific count (e.g., 5 packets).
 6. **Stop**

## **9. Hashing & Integrity**
 1. **Input:** Accept a string or read a file as binary data.
 2. **Compute:** Pass the data through the **SHA-256** algorithm.
 3. **Hexdigest:** Convert the binary hash into a readable hexadecimal string.
 4. **Verification:**
   * Re-calculate the hash of the current data.
   * Compare the new hash with the original stored hash.
   * If they match, the file is unchanged (Integrity verified).
 5. **Stop**

## **10. Data Visualization (Matplotlib & Seaborn)**
 1. **Start**
 2. **Data Prep:** Define lists or numpy arrays for X and Y axes.
 3. **Line Plot:** Connect data points with a line to show trends over time.
 4. **Bar Chart:** Use rectangular bars to compare categories.
 5. **Histogram:** Group numerical data into "bins" to show distribution frequency.
 6. **Scatter Plot:** Plot individual points to see the correlation between variables.
 7. **Heatmap:** Use a color-coded matrix to represent data intensity.
 8. **Render:** Use plt.show() to display all generated graphs.
 9. **Stop**

1.swap
# Input two numbers
num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

# Swapping numbers
temp = num1
num1 = num2
num2 = temp

# Display swapped numbers
print("\nAfter Swapping:")
print("First Number:", num1)
print("Second Number:", num2)

# Check if first number is positive, negative or zero
if num1 > 0:
    print("First number is Positive")

elif num1 < 0:
    print("First number is Negative")

else:
    print("First number is Zero")

2.calculator
# Display menu
print("Simple Calculator")
print("1. Addition")
print("2. Subtraction")
print("3. Multiplication")
print("4. Division")

# Input numbers (float handles integers & decimals)
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

# Input choice
choice = int(input("Enter your choice (1-4): "))

# Perform operations
if choice == 1:
    result = num1 + num2
    print("Result:", result)

elif choice == 2:
    result = num1 - num2
    print("Result:", result)

elif choice == 3:
    result = num1 * num2
    print("Result:", result)

elif choice == 4:
    if num2 != 0:
        result = num1 / num2
        print("Result:", result)
    else:
        print("Error: Division by zero is not allowed")

else:
    print("Invalid choice")

3.factorial fabonacci
# -------- Factorial using Recursion --------

def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

# Input for factorial
num = int(input("Enter a number for factorial: "))

# Display factorial
print("Factorial of", num, "is:", factorial(num))


# -------- Fibonacci using Recursion --------

def fibonacci(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

# Input for Fibonacci
terms = int(input("\nEnter number of Fibonacci terms: "))

print("Fibonacci Sequence:")

for i in range(terms):
    print(fibonacci(i), end=" ")

4.gui tkinter
# Import Tkinter
import tkinter as tk

# Create main window
window = tk.Tk()

# Set window title
window.title("Simple GUI Application")

# Set window size
window.geometry("300x200")

# Function to display message
def show_message():
    user_text = entry.get()
    result_label.config(text="Hello " + user_text)

# Create label
label = tk.Label(window, text="Enter your name:")
label.pack()

# Create entry box
entry = tk.Entry(window)
entry.pack()

# Create button
button = tk.Button(window, text="Submit", command=show_message)
button.pack()

# Label to show result
result_label = tk.Label(window, text="")
result_label.pack()

# Run GUI
window.mainloop()

5.exceptional handling
# exception handling in python

try:
    # Input numbers
    num1 = int(input("Enter first number: "))
    num2 = int(input("Enter second number: "))

    # Perform division
    result = num1 / num2

except ZeroDivisionError:
    print("Error: Division by zero is not allowed")

except ValueError:
    print("Error: Invalid input! Please enter numbers only")

else:
    # Executes if no exception occurs
    print("Result:", result)

finally:
    # Always executes
    print("Program execution completed")

6.nltk
# Import libraries
import nltk

# Download required datasets (run once)
nltk.download('punkt')
nltk.download('wordnet')
nltk.download('vader_lexicon')

from nltk.tokenize import word_tokenize
from nltk.stem import PorterStemmer
from nltk.stem import WordNetLemmatizer
from nltk.sentiment import SentimentIntensityAnalyzer

# Sample text
text = "NLTK is very useful for Natural Language Processing. I love learning NLP!"

# Tokenization
tokens = word_tokenize(text)
print("Tokens:")
print(tokens)

# Stemming
stemmer = PorterStemmer()
stemmed_words = [stemmer.stem(word) for word in tokens]
print("\nStemmed Words:")
print(stemmed_words)

# Lemmatization
lemmatizer = WordNetLemmatizer()
lemmatized_words = [lemmatizer.lemmatize(word) for word in tokens]
print("\nLemmatized Words:")
print(lemmatized_words)

# Sentiment Analysis
sia = SentimentIntensityAnalyzer()
sentiment_score = sia.polarity_scores(text)

print("\nSentiment Analysis:")
print(sentiment_score)

7.web scraper
# Import libraries
import requests
from bs4 import BeautifulSoup

# -------- BeautifulSoup Example --------

# URL of website
url = "https://example.com"

# Send request
response = requests.get(url)

# Parse HTML
soup = BeautifulSoup(response.text, "html.parser")

# Extract title
title = soup.title.text

print("Website Title using BeautifulSoup:")
print(title)


# -------- Selenium Example --------

from selenium import webdriver
from selenium.webdriver.common.by import By
import time

# Open browser (Make sure chromedriver is installed)
driver = webdriver.Chrome()

# Open website
driver.get("https://example.com")

# Wait for page to load
time.sleep(3)

# Extract heading text
heading = driver.find_element(By.TAG_NAME, "h1")

print("\nHeading using Selenium:")
print(heading.text)

# Close browser
driver.quit()

8.scapy pyspark
# Import Scapy library
from scapy.all import sniff, IP

# Function to process packets
def packet_analysis(packet):
    
    # Check if packet contains IP layer
    if packet.haslayer(IP):
        
        # Extract source and destination IP
        src_ip = packet[IP].src
        dest_ip = packet[IP].dst
        
        print("Packet Captured:")
        print("Source IP:", src_ip)
        print("Destination IP:", dest_ip)
        print("---------------------------")

# Capture 5 packets
print("Starting Packet Capture...\n")

sniff(prn=packet_analysis, count=5)

print("\nPacket Capture Completed.")

9.hashes for files
# Import hashlib
import hashlib

# -------- Message Hashing --------

# Input message
message = input("Enter a message: ")

# Generate SHA-256 hash
msg_hash = hashlib.sha256(message.encode())

print("\nGenerated Message Hash:")
print(msg_hash.hexdigest())

# -------- File Hashing --------

# File name (Create sample.txt before running)
file_name = "sample.txt"

# Open file in binary mode
with open(file_name, "rb") as file:
    file_data = file.read()
    
    # Generate file hash
    file_hash = hashlib.sha256(file_data)

print("\nGenerated File Hash:")
print(file_hash.hexdigest())

# -------- Hash Verification --------

print("\nVerifying Hash...")

# Re-generate hash for verification
verify_hash = hashlib.sha256(file_data)

if file_hash.hexdigest() == verify_hash.hexdigest():
    print("File Integrity Verified: Hashes Match")
else:
    print("File Integrity Failed: Hashes Do Not Match")

10.matplotlib
# Import libraries
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np

# Sample cybersecurity data
days = [1, 2, 3, 4, 5]
login_attempts = [50, 75, 40, 90, 60]
attack_types = ["Phishing", "Malware", "DDoS", "Ransomware"]
attack_counts = [20, 35, 15, 25]

# -------- Line Plot --------
plt.figure()
plt.plot(days, login_attempts)
plt.title("Login Attempts Over Days")
plt.xlabel("Days")
plt.ylabel("Login Attempts")
plt.show()

# -------- Bar Chart --------
plt.figure()
plt.bar(attack_types, attack_counts)
plt.title("Number of Cyber Attacks")
plt.xlabel("Attack Types")
plt.ylabel("Count")
plt.show()

# -------- Histogram --------
plt.figure()
traffic_data = np.random.randint(10, 100, 50)
plt.hist(traffic_data)
plt.title("Network Traffic Distribution")
plt.xlabel("Traffic Volume")
plt.ylabel("Frequency")
plt.show()

# -------- Scatter Plot --------
plt.figure()
x = np.random.randint(1, 50, 20)
y = np.random.randint(1, 50, 20)
plt.scatter(x, y)
plt.title("Suspicious Activity Scatter Plot")
plt.xlabel("Source")
plt.ylabel("Destination")
plt.show()

# -------- Heatmap using Seaborn --------
data = np.random.randint(1, 10, (5, 5))

plt.figure()
sns.heatmap(data)
plt.title("Login Activity Heatmap")
plt.show()

Here are the algorithms for each of your Python programs, broken down into logical steps.
## **1. Swapping & Number Check**
 1. **Start**
 2. **Input:** Accept two numbers, num1 and num2.
 3. **Process (Swap):**
   * Store the value of num1 in a temporary variable (temp).
   * Assign the value of num2 to num1.
   * Assign the value of temp to num2.
 4. **Output:** Display the swapped values of num1 and num2.
 5. **Decision:** * If num1 > 0, output "Positive".
   * Else if num1 < 0, output "Negative".
   * Else, output "Zero".
 6. **Stop**
## **2. Simple Calculator**
 1. **Start**
 2. **Display:** Show the menu of operations (1. Add, 2. Sub, 3. Mul, 4. Div).
 3. **Input:** Accept two numbers and an operation choice (1–4).
 4. **Decision (Operations):**
   * If choice is 1: Calculate num1 + num2.
   * If choice is 2: Calculate num1 - num2.
   * If choice is 3: Calculate num1 * num2.
   * If choice is 4:
     * Check if num2 is not zero. If true, calculate num1 / num2.
     * If num2 is zero, output an error message.
 5. **Output:** Display the result of the calculation.
 6. **Stop**
## **3. Factorial & Fibonacci (Recursion)**
**Factorial Algorithm:**
 1. **Define Function:** If n is 0 or 1, return 1 (**Base Case**).
 2. Otherwise, return n * factorial(n - 1) (**Recursive Step**).
 3. **Input:** Accept a number and call the function.
**Fibonacci Algorithm:**
 1. **Define Function:** * If n is 0, return 0.
   * If n is 1, return 1.
   * Otherwise, return fib(n-1) + fib(n-2).
 2. **Loop:** Iterate from 0 to the desired number of terms and call the function for each index.
## **4. GUI with Tkinter**
 1. **Start**
 2. **Initialize:** Create the main application window and set dimensions.
 3. **Create Widgets:** Add a label (instruction), an entry box (input), and a button (action).
 4. **Define Event:** Create a function that:
   * Retrieves text from the entry box.
   * Updates a display label with a "Hello" greeting.
 5. **Main Loop:** Run the application to keep the window open and listen for button clicks.
 6. **Stop**
## **5. Exception Handling**
 1. **Start**
 2. **Try Block:**
   * Input two integers.
   * Attempt to divide the first by the second.
 3. **Except Block:**
   * If the user enters text instead of numbers, catch ValueError.
   * If the second number is zero, catch ZeroDivisionError.
 4. **Else Block:** If no errors occur, display the division result.
 5. **Finally Block:** Always print "Program execution completed."
 6. **Stop**
## **6. NLTK (NLP Processing)**
 1. **Start**
 2. **Setup:** Download necessary NLTK datasets (punkt, wordnet).
 3. **Tokenization:** Break the input sentence into individual words/tokens.
 4. **Stemming:** Strip suffixes from words to get the root form (e.g., "learning" becomes "learn").
 5. **Lemmatization:** Convert words to their dictionary base form using context.
 6. **Sentiment Analysis:** Use the VADER tool to calculate positive, negative, and neutral scores.
 7. **Output:** Display the tokens, stems, lemmas, and sentiment scores.
 8. **Stop**
## **7. Web Scraper (BeautifulSoup & Selenium)**
**BeautifulSoup (Static):**
 1. **Request:** Send an HTTP GET request to the URL.
 2. **Parse:** Convert the raw HTML into a searchable "soup" object.
 3. **Extract:** Find the <title> tag and print its text.
**Selenium (Dynamic):**
 1. **Initialize:** Open a web browser via a driver (e.g., Chrome).
 2. **Navigate:** Go to the specific URL and wait for the page to load.
 3. **Locate:** Find an element (e.g., h1) using the DOM structure.
 4. **Close:** Print the element text and shut down the browser.
## **8. Packet Sniffing (Scapy)**
 1. **Start**
 2. **Define Callback:** Create a function to process every captured packet.
 3. **Filter:** Within the function, check if the packet has an **IP layer**.
 4. **Extract:** Read the Source IP and Destination IP from the packet header.
 5. **Sniff:** Start the capture process for a specific count (e.g., 5 packets).
 6. **Stop**
## **9. Hashing & Integrity**
 1. **Input:** Accept a string or read a file as binary data.
 2. **Compute:** Pass the data through the **SHA-256** algorithm.
 3. **Hexdigest:** Convert the binary hash into a readable hexadecimal string.
 4. **Verification:**
   * Re-calculate the hash of the current data.
   * Compare the new hash with the original stored hash.
   * If they match, the file is unchanged (Integrity verified).
 5. **Stop**
## **10. Data Visualization (Matplotlib & Seaborn)**
 1. **Start**
 2. **Data Prep:** Define lists or numpy arrays for X and Y axes.
 3. **Line Plot:** Connect data points with a line to show trends over time.
 4. **Bar Chart:** Use rectangular bars to compare categories.
 5. **Histogram:** Group numerical data into "bins" to show distribution frequency.
 6. **Scatter Plot:** Plot individual points to see the correlation between variables.
 7. **Heatmap:** Use a color-coded matrix to represent data intensity.
 8. **Render:** Use plt.show() to display all generated graphs.
 9. **Stop**

```
