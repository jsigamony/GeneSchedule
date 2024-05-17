Loading and Cleaning the Data:
• The code starts by loading a list of course details from an Excel file
into a table (or DataFrame) using a library called pandas.
• I removed the first three rows of the course allocation sheet table
because these rows were not useful data (they contained headers).
• The code then changes the names of some unnamed columns to
things like 'Course-Code', 'Course Name', etc., to make them more
understandable.
• Lastly, any rows that had NaN values are removed to keep the data
tidy and complete.
•
2. Setting Up for the Algorithm:
• The script sets up some variables like time slots and room numbers
which represent when and where the classes can happen.
• It defines some settings for the genetic algorithm—this is a technique
that tries to find the best solution to a problem by mimicking natural
evolution (like survival of the fittest).
3. The Genetic Algorithm – Making a Timetable:
• Fitness Function: This part checks how good a timetable is. A
timetable gets a lower score if it has issues like a teacher scheduled
in two places at once, or a room double-booked. This also checks for
other clashes as well.
• Create Individual: This creates one possible timetable by randomly
assigning courses to times and rooms.
• Crossover: This is like genetic mixing—you take two timetables and
combine them to make a new one, hoping it might inherit the best
features of both.
• Mutate: This introduces random changes to a timetable, like
changing a course's room or time, to explore different possibilities.
• Selection: This picks the best timetables out of a small random
group, again mimicking natural selection.
4. Running the Algorithm:
• The script creates a bunch of random timetables and then keeps
improving them through the crossover and mutation steps, trying to
find the best possible timetable over many rounds (or generations).
• At the end, it chooses the timetable that works the best—where
courses don’t clash, and rooms and teachers are scheduled
efficiently.
5. Final Output:
• The best timetable is converted back into a dataframe table format
so it’s easy to look at and use.
