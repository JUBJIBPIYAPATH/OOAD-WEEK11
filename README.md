# OOAD-WEEK11
State Diagram
```
1.เครื่อขายตั๋วรถไฟ

[*] -> User 
User --> TicketMachine : ChooseStation
User --> TicketMachine : InsertMoney 
TicketMachine --> Display : Showcost
TicketMachine --> TicketMachine : checkMoney 
TicketMachine --> User : printTicket
User --> [*] : printTicket
User --> [*] : returnmoney

```
![](https://github.com/JUBJIBPIYAPATH/OOAD-WEEK11/blob/master/S1.PNG?raw=true)

```
2.ล็อกอินและล็อคเอ้าท์
(*) --> "Login"
--> "SignOut"
--> (*)
```
![](https://github.com/JUBJIBPIYAPATH/OOAD-WEEK11/blob/master/S2.PNG?raw=true)

```
3.เครื่องกดเงิน
state "Card Slots" as cardslots
state "Enter Amount" as enteramount
state "Money Slots" as moneyslots
[*] --> cardslots : wait insert the card
cardslots --> Keypad : Keypad successfully
Keypad --> enteramount : Select amount money
enteramount --> moneyslots : accept money
moneyslots --> [*] : accept card
```
![](https://github.com/JUBJIBPIYAPATH/OOAD-WEEK11/blob/master/S3.PNG?raw=true)

```
4.เข้ารหัสผ่านเว็บไซส์
[*] -> user 
user -up-> LoginPage : InsertNameAndPass
LoginPage -> WebDatabase : CheckNameandPass
WebDatabase -down-> user : SHowIncorrect
WebDatabase -down-> user : enterpage
user -> [*] : enterpage
user -> [*] : SHowIncorrect
```
![](https://github.com/JUBJIBPIYAPATH/OOAD-WEEK11/blob/master/S4.PNG?raw=true)

```
5.เปิดปิดไฟ 
[*] -r-> on :install
on -r-> off
off -r-> on
```
![](https://github.com/JUBJIBPIYAPATH/OOAD-WEEK11/blob/master/S5.PNG?raw=true)

#Activity Diagram

```
1.
(*) --> Login
if "" then
-r-> Member
else
-r-> Register
-r-> Member
Member -r-> Website 
Website -up-> Logout
Logout -up-> (*)
```
![](https://github.com/JUBJIBPIYAPATH/OOAD-WEEK11/blob/master/A1.PNG?raw=true)

```
2.
(*) --> "Postman"
Postman -d-> delivery 

if "  postman come delivery\nand recipient...." then
-l->[stay at home] "Send success"
-up->[End] (*)  

else
-r->[Not at home] "Resend"
Resend -u-> delivery
endif
```
![](https://github.com/JUBJIBPIYAPATH/OOAD-WEEK11/blob/master/A2.PNG?raw=true)

```
3.
(*) -> user 
user  -down-> MachineCheckIDCar 

MachineCheckIDCar -> database 
database -> Display
Display -> user 
database -> cuttingFundSystem 
if "money>totalcharges" then 
-->[true] "cuttingMonney"
  --> sentSMS
  -->(*)
 else
 ->[false]"Can'tcuttingMonney"
 --> sentSMS
-->(*)
```
![](https://github.com/JUBJIBPIYAPATH/OOAD-WEEK11/blob/master/A3.PNG?raw=true)

```
4.
(*) ->   "direct"   

if "expressway" then
-->[true] "expressway"

--> "pay tolls"   
  --right-> (*)
else
->[false] "traffic jam"   

-r->[long time] (*)
endif
```
![]()
