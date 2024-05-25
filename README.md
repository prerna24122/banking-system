# banking-system
<!DOCTYPE html>
<html>
    <head>
        <title> bank system</title>
    </head>
    <body>
        <script>
            class bank{
                constructor(nm,account_number,balance){ //constructor means properties of class
                    this.name=nm;
                    this.account_number=account_number;
                    this.balance=balance;
                }
                withdraw(amount){ //withdraw function
                    this.balance-=amount;
                   console.log("withdraw successfull!");
                    
                }
                deposite(amount){ //deposit function

                    this.balance+=amount
                    console.log("deposit successfully!");
                }
                all_details(){   //all details
                    console.log("================Full Details of Account=========\n");
                    console.log("name: "+ this.name +"\nAccount number : " + this.account_number +"\nbalance : " +this.balance );

                }
                last_transjection(){

                }
            }
            var nm=prompt("enter the name");
            var account_number=parseInt(prompt("enter the account number"))
            var balance=parseInt(prompt("enter the balance"))
            var b=new bank(nm,account_number,balance);  // class object


            function mybank(){  // main function
            var key=parseInt(prompt("enter either want to deposit , withdraw, or want to see details :")) 
            switch(key){
                case 1:
                    var amount=parseInt(prompt("enter the amount deposit:"));
                    b.deposite(amount);
                    break;
                case 2:
                    var amount=parseInt(prompt("enter the amount withdraw: "));
                    b.withdraw(amount); 
                    break;
                case 3:
                   b.all_details();
                   break;

            }   
    
         }
            setInterval(mybank,1000); //repeat the function
        </script>
    </body>
</html>
