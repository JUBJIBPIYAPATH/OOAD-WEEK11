# OOAD-WEEK11
State Diagram
```
เครื่อขายตั๋วรถไฟ

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
