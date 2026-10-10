# Test Cases – Selenium Web Automation

**Project:** Movie Ticket Booking Web Automation
**Application:** [PracticeQA Automation – Tickets](https://www.practiceqaautomation.com/tickets)
**Automation Tool:** Selenium WebDriver
**Programming Language:** Python

## 1. Page Loading and Navigation

| Test Case ID | Test Case Name                 | Short Description                                                  |
| ------------ | ------------------------------ | ------------------------------------------------------------------ |
| TC01         | Verify Application Launch      | Verify that the ticket booking application opens successfully.     |
| TC02         | Verify Page Title              | Check whether the page title matches the expected title.           |
| TC03         | Verify Current URL             | Verify that the browser opens the expected application URL.        |
| TC04         | Verify Page Content            | Check whether the main page content is displayed.                  |
| TC05         | Verify Page Element Visibility | Verify that essential booking elements are visible.                |
| TC06         | Verify Date Selection Options  | Check whether available date options are displayed.                |
| TC07         | Verify City Dropdown           | Verify that the city selection control is available.               |
| TC08         | Verify Language Dropdown       | Verify that the language selection control is available.           |
| TC09         | Verify Genre Options           | Check whether movie genre options are available.                   |
| TC10         | Verify Initial Booking State   | Verify that the booking page displays its initial state correctly. |

## 2. Date, City, Language and Genre Selection

| Test Case ID | Test Case Name                   | Short Description                                            |
| ------------ | -------------------------------- | ------------------------------------------------------------ |
| TC11         | Select Booking Date              | Select the required date for the booking.                    |
| TC12         | Verify Selected Date             | Verify that the chosen date is reflected in the interface.   |
| TC13         | Select City                      | Select a city from the available city options.               |
| TC14         | Verify Selected City             | Check whether the selected city is retained.                 |
| TC15         | Select Movie Language            | Select the required movie language.                          |
| TC16         | Verify Selected Language         | Verify that the selected language is applied.                |
| TC17         | Select Movie Genre               | Choose a movie genre from the available options.             |
| TC18         | Verify Selected Genre            | Verify that the selected genre is retained.                  |
| TC19         | Change Booking Filters           | Change the selected date or other available filters.         |
| TC20         | Verify Combined Filter Selection | Verify the selected date, city, language and genre together. |

## 3. Movie and Showtime Selection

| Test Case ID | Test Case Name               | Short Description                                                          |
| ------------ | ---------------------------- | -------------------------------------------------------------------------- |
| TC21         | Verify Movie Listings        | Check whether matching movie listings are displayed.                       |
| TC22         | Verify Movie Details         | Verify the displayed details of a listed movie.                            |
| TC23         | Select a Movie               | Select a movie from the available listings.                                |
| TC24         | Verify Available Showtimes   | Check whether showtimes are displayed for the selected movie.              |
| TC25         | Select a Showtime            | Select an available showtime.                                              |
| TC26         | Verify Selected Showtime     | Verify that the selected showtime is correctly reflected.                  |
| TC27         | Change Selected Movie        | Select another movie when the application allows it.                       |
| TC28         | Verify Showtime Availability | Verify that the selected movie has an available showtime.                  |
| TC29         | Verify No Matching Results   | Check the application's behavior when no matching listings are available.  |
| TC30         | Verify Booking Progression   | Verify that the user can proceed after completing the required selections. |

## 4. Seat Selection

| Test Case ID | Test Case Name                   | Short Description                                                   |
| ------------ | -------------------------------- | ------------------------------------------------------------------- |
| TC31         | Verify Seat Selection Page       | Verify that the seat selection interface opens.                     |
| TC32         | Verify Seat Layout               | Check whether the seat layout is displayed.                         |
| TC33         | Verify Seat Availability         | Identify available and unavailable seats where indicated.           |
| TC34         | Select a Seat                    | Select an available seat.                                           |
| TC35         | Verify Selected Seat             | Verify that the selected seat is visibly marked.                    |
| TC36         | Select Multiple Seats            | Select multiple seats if the application supports it.               |
| TC37         | Verify Seat Selection Count      | Verify the number of selected seats.                                |
| TC38         | Deselect a Seat                  | Remove a previously selected seat.                                  |
| TC39         | Verify Unavailable Seat Handling | Check whether unavailable seats can be selected.                    |
| TC40         | Continue After Seat Selection    | Verify that the user can proceed after the required seat selection. |

## 5. Customer and Contact Details

| Test Case ID | Test Case Name                 | Short Description                                                    |
| ------------ | ------------------------------ | -------------------------------------------------------------------- |
| TC41         | Verify Contact Details Form    | Verify that the customer details form is displayed.                  |
| TC42         | Enter Customer Name            | Enter a name in the relevant input field.                            |
| TC43         | Enter Email Address            | Enter an email address in the relevant input field.                  |
| TC44         | Enter Mobile Number            | Enter a mobile number in the relevant input field.                   |
| TC45         | Verify Entered Details         | Verify that entered customer information is retained.                |
| TC46         | Validate Empty Required Fields | Check how the application handles missing required details.          |
| TC47         | Validate Invalid Email Address | Check whether an invalid email address is rejected.                  |
| TC48         | Validate Invalid Mobile Number | Check how the application handles an invalid mobile number.          |
| TC49         | Verify Contact Form Submission | Verify that valid customer details can be submitted.                 |
| TC50         | Continue to Next Booking Step  | Verify progression after the required customer details are provided. |

## 6. Snacks and Booking Summary

| Test Case ID | Test Case Name                  | Short Description                                                               |
| ------------ | ------------------------------- | ------------------------------------------------------------------------------- |
| TC51         | Verify Snack Selection Page     | Verify that the snack selection interface is displayed, if available.           |
| TC52         | Verify Available Snacks         | Check whether the available snack options are displayed.                        |
| TC53         | Select a Snack                  | Select a snack from the available options.                                      |
| TC54         | Update Snack Quantity           | Change the quantity of a selected snack, if supported.                          |
| TC55         | Remove a Selected Snack         | Remove a previously selected snack, if supported.                               |
| TC56         | Verify Snack Price              | Verify the displayed price of a selected snack.                                 |
| TC57         | Verify Booking Summary          | Check the displayed summary of the selected booking.                            |
| TC58         | Verify Ticket Price Calculation | Verify the ticket subtotal based on the selected seats.                         |
| TC59         | Verify Total Booking Amount     | Check whether the displayed total reflects applicable ticket and snack charges. |
| TC60         | Continue to Payment             | Verify that the user can proceed to the payment stage.                          |

## 7. Payment, OTP and Booking Completion

| Test Case ID | Test Case Name                         | Short Description                                                                                         |
| ------------ | -------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| TC61         | Verify Payment Page                    | Verify that the payment interface opens.                                                                  |
| TC62         | Navigate Back and Verify Previous Page | Navigate back and verify that the expected previous page loads.                                           |
| TC63         | Verify Payment Method                  | Check whether the expected payment method is available.                                                   |
| TC64         | Enter Card Details                     | Enter the required card information in the applicable fields.                                             |
| TC65         | Validate Missing Card Details          | Check how the application handles incomplete card information.                                            |
| TC66         | Validate Invalid Card Details          | Verify the application's handling of invalid card input.                                                  |
| TC67         | Verify OTP Interface                   | Verify that the OTP entry interface is displayed when required.                                           |
| TC68         | Validate OTP Submission                | Check the application's response to valid or invalid OTP input, where testable.                           |
| TC69         | Verify Booking Confirmation            | Verify that a successful booking displays the expected confirmation.                                      |
| TC70         | Verify Ticket Download                 | Verify that the ticket can be downloaded or that the expected download action is available after booking. |

## Test Execution Status

| Status         | Meaning                                                                          |
| -------------- | -------------------------------------------------------------------------------- |
| Not Run        | The test has not been executed.                                                  |
| Pass           | The actual result matches the expected result.                                   |
| Fail           | The actual result differs from the expected result.                              |
| Blocked        | The test cannot be executed because a prerequisite or dependency is unavailable. |
| Not Applicable | The test does not apply to the application's available functionality.            |

**Note:** This is the proposed master test case index. Confirm each scenario against the actual application and your existing scripts before marking it as completed. Conditional features, such as multiple-seat selection, snacks, OTP, and ticket download, should only be retained if supported by the website.
