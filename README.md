<table>
<tr><td>

|  Identifying States |         
|---|
|  Sign Up Page |
|  Log In Page |
|  Logged In Page |

</td><td>

|  Identifying Events |
|---|
|  User signs up |
|  User logs in |
|  User logs out |

</td></tr> </table>

<br>


---
title: Simple sample
---
```mermaid
stateDiagram-v2
    [*] --> Still
    Still --> [*]

    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
```

```mermaid
stateDiagram
    Sign_Up_Page --> Sign_Up_Page: Invalid signup details
    Sign_Up_Page --> Log_In_Page: User signs-in
    Log_In_Page --> Log_In_Page: Incorrect login details
    Log_In_Page --> Users_is_logged_into_the_site(Logged_In_Page): User logs in
    Users_is_logged_into_the_site(Logged_In_Page) --> Log_In_Page: User logs out
```


####  State transition table:

|  Initial State | Event  | Next State  |
|---|---|---|
|  Sign-up Page |  Invalid signup details | Sign-up Page  |
|  Sign-up Page |  User signs up | Log In Page  |
|  Log In Page |  Incorrect login details | Log In Page  |
|  Log In Page |  User logs in |  User is logged into the site (Logged In Page) |
|  Logged In page | User logs out  | Log In Page  |

<br>

#### <u>Test case for states and events/transitions:</u>
* Start: Sign-up Page
* Signs up => Log In Page
* Log in => User is logged into the site(Logged In Page)
* Log out => Log In Page

