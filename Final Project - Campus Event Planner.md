- Instructions
	- Should keep track of multiple events
	- Store information about each event (name, date location, capacity, cost per attendee, etc.)
	- Estimate total revenue if the event sells out.
	- Allow the user to interact with a menu to:
		- Add new events
		- View all events
		- Search for events
		- Remove events
		- Get summary statistics (like most expensive event, total possible revenue, etc.)


## Possible feature adds
- [ ] Input verification
- [ ] Edit event
- [ ] Day of the week calculator 


## WIP Thoughts
- [ ] Using f string for formatting on line 31
- [ ] How could I contend with multiple "most expensive events" maybe an array?
- [ ] Nested loops for searching nested dicts so that I can search by any of the events attributes
- [ ] Date Verification make sure that the format of the date is MM/DD/YYYY
	- [ ] For Month the number should not exceed 12
	- [ ] I would need to add verification for each of the number of days in each month most likely nested for loops
	- [ ] 