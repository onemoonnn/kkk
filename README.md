This is a Java project where I implemented my own Date class to work with calendar dates. I wanted to try building a date utility from scratch instead of relying on Java’s built-in LocalDate, just to get a better understanding of how dates actually work, including leap years, date validation, and calculating day differences.

The class has three main attributes — day, month, and year — and it checks that the date is valid when creating or updating it. That means things like not allowing February 30th, and handling leap years correctly (e.g., Feb 29 is valid in 2024 but not in 2023). There's a method called isValidDate that handles all of that.

I also added a method to get the day of the week (like “Monday” or “Friday”) using Java’s Calendar, and another method that calculates the number of days between two dates. It uses GregorianCalendar under the hood to handle leap years and other calendar quirks automatically.

The class implements Comparable<Date>, so I can sort a list of dates in ascending order (by year, then month, then day). This is useful if you have a bunch of dates and want to organize them chronologically.

The printDate method prints the date in a readable format like “March 5, 2023” instead of numeric form. There's also an updateDate method which lets you change the date after it's created, but it only works if the new date is valid — otherwise, it gives an error message.

In the Main class, I wrote a few test cases. It creates a few Date objects (some of them valid, some invalid to test error handling), prints one of the dates and its day of the week, calculates the number of days between two dates, sorts a list of dates, and tries to update a date with invalid input to show how that’s handled.

To run the program, you just compile Date.java and Main.java, and run the Main class. It’s all console-based and doesn’t require any additional libraries. Overall, it was a fun way to practice object-oriented programming in Java and get more comfortable with date logic and using Java’s built-in calendar tools.
