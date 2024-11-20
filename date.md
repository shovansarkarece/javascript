# JAVASCRIPT DATE OBJECT

![image](https://github.com/user-attachments/assets/e6483aad-c29a-4b0e-b47c-fc0e03d9b6f5)

![image](https://github.com/user-attachments/assets/feffa2de-bb73-4a4a-98d1-66b7d77b83cf)
### Syntax:
- **`new Date()`**
- **`new Date(date string)`**
- **`new Date(year,month)`**
- **`new Date(year,month,day)`**
- **`new Date(year,month,day,hours)`**
- **`new Date(year,month,day,hours,minutes)`**
- **`new Date(year,month,day,hours,minutes,seconds)`**
- **`new Date(year,month,day,hours,minutes,seconds,ms)`**
- **`new Date(milliseconds)`**
## The JavaScript date object can be used to get year, month and day.
- **JavaScript counts months from 0 to 11.January = 0, and December = 11
### 1.Current date and time
- **`new Date()`: Creates a Date object representing the current date and time.**
```
// const currentDate = new Date();
// console.log(currentDate);
//This is the ISO 8601 format, which is a standard for representing dates and times. In this format, the date and time are represented together, separated by the letter "T".
The "Z" at the end indicates that the time is in UTC (Coordinated Universal Time).But when you run on browser it will return more human-readable format.
```
### 2.`new Date(dateString)`: 
- **Creates a Date object based on the provided date string.**
```
// const dateString = "2024-02-19T10:44:09.274Z";
// const dateFromString = new Date(dateString);
// console.log(dateFromString);
```
### 3.`new Date(year, month)`: 
- **Creates a Date object with the specified year and month.**
```
// const date1 = new Date(2025, 12);
// console.log(date1);
```
### 4.`new Date(year, month, day)`: 
- **Creates a Date object with the specified year, month, and day.**
```
// const date2 = new Date(2024, 1, 19);
// console.log(date2);
```
### 5.`new Date(year, month, day, hours)`: 
- **Creates a Date object with the specified year, month, day, and hours.**
```
// const date3 = new Date(2024, 1, 19, 10);
// console.log(date3);
```
### 6.`new Date(year, month, day, hours, minutes)`: 
- **Creates a Date object with the specified year, month, day, hours, and minutes.**
```
// const date4 = new Date(2024, 1, 19, 10, 44);
// console.log(date4);
```
### 7.`new Date(year, month, day, hours, minutes, seconds)`: 
- **Creates a Date object with the specified year, month, day, hours, minutes, and seconds.**
```
// const date5 = new Date(2024, 1, 19, 10, 44, 9);
// console.log(date5);
```
### 8.`new Date(year, month, day, hours, minutes, seconds, ms)`: 
- **Creates a Date object with the specified year, month, day, hours, minutes, seconds, and milliseconds.**
```
// const date6 = new Date(2024, 1, 19, 10, 44, 9, 274);
// console.log(date6);
```
### 9.`new Date(milliseconds)`: 
- **Creates a Date object representing the number of milliseconds since the Unix epoch (January 1, 1970, 00:00:00 UTC).**
```
const curMilliSeconds = new Date().getTime();
console.log(curMilliSeconds)
// const milliseconds = 1632090690883; // Example milliseconds
const dateFromMilliseconds = new Date(curMilliSeconds);
console.log(dateFromMilliseconds);
```
### Date String Format(Important): 
- **If the dateString is in a recognizable format, the Date object will be created accordingly.**
```
new Date(date string) creates a date object from a date string
// const date1 = new Date("2024-01-05"); // Year-Month-Day
// const date2 = new Date("January 5, 2024"); // Month Day, Year
// console.log(date1);//////Output:=====>2024-01-05T00:00:00.000Z
// console.log(date2);//////Output:=====>2024-01-04T23:00:00.000Z
```
### In JavaScript, the first day of the week (day 0) is Sunday.
- **day of the week (0 for Sunday, 1 for Monday, ..., 6 for Saturday)**
## getDate()
>It returns the integer value between 1 and 31 that represents the day for the specified date on the basis of local time.
```
let date=new Date()
console.log(date.getDate())
```
## getDay()
>It returns the integer value between 0 and 6 that represents the day of the week on the basis of local time.
```
let date=new Date()
console.log(date.getDay())
```
## getFullYears()
>It returns the integer value that represents the year on the basis of local time.
```
let date=new Date()
console.log(date.getFullYear())
```
## getHours()
>It returns the integer value between 0 and 23 that represents the hours on the basis of local time.
```
let date=new Date()
console.log(date.getHours())
```
## getMilliseconds()
>It returns the integer value between 0 and 999 that represents the milliseconds on the basis of local time.
```
let date=new Date()
console.log(date.getMilliseconds())
```
## getMinutes()
>It returns the integer value between 0 and 59 that represents the minutes on the basis of local time.
```
let date=new Date()
console.log(date.getMinutes())
```
## getMonth()
>It returns the integer value between 0 and 11 that represents the month on the basis of local time.
```
let date=new Date()
console.log(date.getMonth())
```
## getSeconds()
>It returns the integer value between 0 and 60 that represents the seconds on the basis of local time.
```
let date=new Date()
console.log(date.getSeconds())
```
## getUTCDate()
>It returns the integer value between 1 and 31 that represents the day for the specified date on the basis of universal time.
```
let date=new Date()
console.log(date.getUTCDate())
```
## getUTCDay()
>It returns the integer value between 0 and 6 that represents the day of the week on the basis of universal time.
```
let date=new Date()
console.log(date.getUTCDay())
```
## getUTCFullYears()
>It returns the integer value that represents the year on the basis of universal time.
```
let date=new Date()
console.log(date.getUTCFullYear())
```
## getUTCHours()
>It returns the integer value between 0 and 23 that represents the hours on the basis of universal time.
```
let date=new Date()
console.log(date.getUTCHours())
```
## getUTCMinutes()
>It returns the integer value between 0 and 59 that represents the minutes on the basis of universal time.
```
let date=new Date()
console.log(date.getUTCMinutes())
```
## getUTCMonth()
>It returns the integer value between 0 and 11 that represents the month on the basis of universal time.
```
let date=new Date()
console.log(date.getUTCMonth())
```
### Combined example of get() method
```
const currentDate = new Date();
//// In a date object, the time is static.
const year = currentDate.getFullYear();
console.log(year)
const month = currentDate.getMonth(); // 0-based index
console.log(month)
const date = currentDate.getDate();
console.log(date)
const day = currentDate.getDay();
console.log(currentDate);
console.log(day);
```
