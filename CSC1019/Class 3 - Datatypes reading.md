## Avalible modules 
- Module calendar
	- General calendar related functions
- Module time
	- time access and conversions 
- Module zoneinfo
	- concrete time zones representing the IANA time zone database.
- Package dateutil 
	- Third-party library with expanded timezones and parsing support
- Package DataType
	- Third-party library that introduces distinct static types to allow static type checkers to differentiate between naive and aware datetimes
## Aware and Naive Objects
- difference is whether or not they include time zone info
- with enough knowledge of applicable algorithmic and political time adjustments, such as time zone and daylight saving time info and #awareObject can locate itself relative to another #awareObject 
- Aware represents a specific moment in time that is not open to interpretation
- #naiveObject doesn't contain enough info to unambiguously locate itself relative to other date/time objects
	- These are easier to work with at the cost of realities
- datetime and time objects have an optional time zone info attribute
	- tzinfo: instance of a subclass of the abstract tzinfo class
	- these capture info about the offset form UTC time, the time zone name, and whether daylight savings is in effect
### Date time Constants
- datetime exports the following constants
	- datetime.MINYEAR
		- The smallest year number allowed in a data or datetime object.     MINYEAR = 1
	- datetime.MAXEAR
		- The biggest year number allowed.                                                         MAXYEAR = 9999
	- datetime.UTC
		- Alias for UTC time zone singleton date.timezone.utc
### Date time types
class