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

//* JavaScript Get Date Methods / Getting Components:
//* ===================================================

// You can get various components of a date using the methods of the Date object:
// const currentDate = new Date();
// // //? In a date object, the time is static.
// const year = currentDate.getFullYear();
// console.log(year)
// const month = currentDate.getMonth(); // 0-based index
// console.log(month)
// const date = currentDate.getDate();
// console.log(date)
// const day = currentDate.getDay();
// console.log(currentDate);
// console.log(day);
// In JavaScript, the first day of the week (day 0) is Sunday.
// day of the week (0 for Sunday, 1 for Monday, ..., 6 for Saturday)




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
// const currentTime = new Date();
// const hours = currentTime.getHours();
// const minutes = currentTime.getMinutes();
// const seconds = currentTime.getSeconds();
// const time = currentTime.getTime();
// console.log(time);
```

# Set Time Methods:
## `setHours(hourValue[, minuteValue[, secondValue[, millisecondValue]]])`: 
- **Sets the hours for a specified date according to local time.**
```
// const date = new Date();
// date.setHours(10);
// console.log(date); // Date object with the hours set to 10
```
## `setMinutes(minuteValue[, secondValue[, millisecondValue]])`: 
- **Sets the minutes for a specified date according to local time.**
```
// const date = new Date();
// date.setMinutes(30);
// console.log(date); // Date object with the minutes set to 30
```
## `setSeconds(secondValue[, millisecondValue])`: 
- **Sets the seconds for a specified date according to local time.**
```
// const date = new Date();
// date.setSeconds(45);
// console.log(date); // Date object with the seconds set to 45
```
## `setMilliseconds(millisecondValue)`: 
- **Sets the milliseconds for a specified date according to local time.**
```
// const date = new Date();
// date.setMilliseconds(500);
// console.log(date); // Date object with the milliseconds set to 500
```
## `setTime(timeValue)`: 
- **Sets the Date object to the time represented by a number of milliseconds since January 1, 1970, 00:00:00 UTC.**
```
const date = new Date();
date.setTime(1832090690883);
console.log(date);
```
## All Output below here:
![image](https://github.com/user-attachments/assets/ec91db0b-14e6-4855-a098-9ff6a3befcb2)
# A few useful methods of the Date object in JavaScript
## 1.toLocaleString(): 
- **Returns a string representing the date and time portion of a Date object using the current locale's conventions.**
```
// const date = new Date();
// const localString = date.toLocaleString();
// console.log(localString);
// Example output: "2/19/2024, 4:30:00 PM" (depending on the locale)
```
### Output:
![image](https://github.com/user-attachments/assets/f4539d4d-f80c-4c1a-b11b-b09649a77ddd)

## 2.toLocaleDateString(): 
- **Returns a string representing the date portion of a Date object using the current locale's conventions.**
```
// const date = new Date();
// const localDateString = date.toLocaleDateString();
// console.log(localDateString);
// Example output: "2/19/2024" (depending on the locale)
```
### Output:
![image](https://github.com/user-attachments/assets/b5bf7261-7a99-4d82-940c-e74f79d979aa)

## 3.toLocaleTimeString(): 
- **Returns a string representing the time portion of a Date object using the current locale's conventions.**
```
// const date = new Date();
// const localTimeString = date.toLocaleTimeString();
// console.log(localTimeString);
// Example output: "4:30:00 PM" (depending on the locale)
```
### Output:
![image](https://github.com/user-attachments/assets/d4575b87-e935-424d-9db6-bb4707febe44)
## 5.parse(): 
- **Parses a string representation of a date and returns the number of milliseconds since January 1, 1970, 00:00:00 UTC.**
```
// const dateString = "2024-02-19T16:30:00Z";
// const parsedDate = Date.parse(dateString);
// console.log(parsedDate); // Example output: 1703254200000 (milliseconds)
```
### Output:
![image](https://github.com/user-attachments/assets/b0224ee8-c6ad-43c1-a8a9-1767c8946b4f)
## Date.now() 
- **It is a static method of the Date object.**
- **Use Date.now() if you want the timestamp right this second.**
- **It returns the current timestamp (number of milliseconds) representing the current moment.**
- **Use new Date().getTime() if you have an existing Date object from elsewhere and want its timestamp.**
```
// let newDate = new Date();
// console.log(Date.now());
// console.log(newDate.getTime());
```
### Outpt:
![image](https://github.com/user-attachments/assets/798818d0-bd79-4413-a1b4-d799759bf7b6)
# Interview Questions
## 1.Write a function to add a specified number of days to a given date.
```
// const addDaysToDate = (date, extraDay) => {
//     // console.log(date);
//     // console.log(date.setDate(date.getDate() + extraDay));
//     // console.log(new Date(1709769600000));
//   let updatedDate = date.setDate(date.getDate() + extraDay);
//   return new Date(updatedDate);
// };

// // // Example usage:
// const date = new Date("2024-02-29");
// const newDate = addDaysToDate(date, 7);
// console.log(newDate);
// console.log(newDate.toLocaleDateString());
```
## 2.Write a function to calculate the difference in days between two given dates.
```
const getDaysDifference = (d1, d2) => {
  let oneDay = 24 * 60 * 60 * 1000;
  let diff = Math.abs(d1 - d2);
  return Math.round(diff / oneDay);
};
// Example usage:
const date1 = new Date("2024-02-19");
const date2 = new Date("2024-03-01");
console.log(getDaysDifference(date1, date2)); // Output: 11 (difference in days)
```
