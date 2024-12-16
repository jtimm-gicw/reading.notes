# 201-Read_13

## Local Storage and How To Use It On Websites

1. Why would a developer use local storage for a web application?
A developer might use local storage for a web application for several reasons, as it provides a way to store data directly in the browser with certain advantages:
*Persistent Data Storage*
**Local storage** retains data even after the browser is closed and reopened, unlike session storage, which clears data when the session ends.
This is ideal for storing user preferences, settings, or data that should persist between sessions without needing to communicate with the server.

*Improved Performance*
Retrieving data from local storage is faster than making a server request, as the data is already stored in the user's browser.
Reduces server load and bandwidth usage.
*Simplified Offline Access*
Local storage enables applications to function offline by storing necessary data (e.g., cached resources or form inputs).
This is especially useful for progressive web apps (PWAs) or apps with offline capabilities.
*No Server Dependency*
Developers can use local storage to temporarily store data without needing to set up a backend or database, which is useful for small-scale projects or prototypes.
*Ease of Use*
Local storage has a simple API (`localStorage.setItem, localStorage.getItem`, etc.) and doesn’t require external libraries or databases.
It’s easier to implement compared to other storage solutions like cookies or IndexedDB.

2. What information should not be stored in local storage?
* Sensitive Personal Information (PII)
* Authentication Data
* Financial Information
* Highly Confidential Business Data
* Large Datasets
* Data Requiring Expiration
* Private Health Information (PHI)
* Encrypted Data (if relying solely on JavaScript)

3. Local storage can store what type of data? How would you convert it to that type before storing?
Local storage in a web browser stores data as *strings*, which means any data type must be converted into a string before storing and then parsed back to its original type when retrieved. 
- Always convert data into a string format before storing.
- Use JSON for structured data like objects and arrays.
- Be mindful of type conversion during both storing and retrieving to maintain consistency.









