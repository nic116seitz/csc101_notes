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


## Required Adds
- [ ] Class design
	- [ ] Attributes
		- [x] Name (string)
		- [x] date (string or other simple format)
		- [x] location (string)
		- [x] capacity(int max number of attendees)
		- [x] price_per_person(float)
		- [x] Tags
	- [ ] Methods 
		- [x] init
		- [ ] String description of the event
		- [ ] Compute potential rev for the event if the event sells out
- [ ] Data storage
	- [ ] List of event objects
	- [ ] **Optional**
		- [ ] Use tuples where appropriate
			- [ ] Tuple of allowed event cats
			- [ ] Tuple of valid locations or time slots
	- [ ] Students must add access and iterate over this list in meaningful ways
- [ ] Functions
	- [ ] display menu()
	- [ ] Add_events(events_list)
	- [ ] list_events(events_list)
	- [ ] find_event_by_name(events_list, search_name) - must be partial or full match
	- [ ] remove_event(event_list) - remove by index or name
	- [ ] Show_summary(events_list) - see below
- [ ] Menu and Program Flow
	- [ ] Must use a loop until the user chooses to quit
- [ ] Input validation
	- [ ] Ensure capacity is non-negative int
	- [ ] Ensure price is a non-negative number
	- [ ] Ensure menu choices are within range
	- [ ] If invalid input is entered use branching to show:
		- [ ] Error message
		- [ ] Ask again or return to menu
- [ ] Loops
	- [ ] Use at least one main loop for the menu
	- [ ] Use at least one additional loop, such as:
		- [ ] Looping over
## Possible feature adds
- [ ] Input verification
- [ ] Edit event
- [ ] Day of the week calculator 
- [ ] For date verification


## WIP Thoughts
- [ ] Using f string for formatting on line 31
- [ ] How could I contend with multiple "most expensive events" maybe an array?
- [ ] Nested loops for searching nested dicts so that I can search by any of the events attributes
- [ ] Date Verification make sure that the format of the date is MM/DD/YYYY
	- [ ] For Month the number should not exceed 12
	- [ ] I would need to add verification for each of the number of days in each month most likely nested for loops
- [ ] The events list should be a dict to avoid the possibility of having duplicate events