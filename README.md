 public static void main(String[] args) {

        Scanner s = new Scanner(System.in);
       //1.Write a program that prints the numbers from 1 to 100 such that:
        System.out.println("Q1");
        for(int i=1;i<=100;i++){
            if(i%3==0&&i%5==0){
                System.out.println("FizzBuzz");
            }
            else if(i%3==0){
                System.out.println("Fizz");
                continue;
            } else if (i%5==0) {
                System.out.println("Buzz");
            }
            System.out.println(i);
        }

        //2.Write a Java program to reverse a string.
        System.out.println("Q2");
        System.out.println("Enter the word");
       // String str=s.nextLine();
        String str=s.nextLine();
        for(int i=str.length()-1;i>=0;i--){
            System.out.print(str.charAt(i));
        }
        System.out.println();



        //3.Write a program that prompts the user to input a positive integer. It should then print the multiplication table of that number.
        System.out.println("Q3");
        System.out.println("Please Enter Postive number");
        int pos=s.nextInt();
        if(pos<0){
            System.out.println("Postive Just ");
        }
        for(int i=1;i<=10;i++){
            System.out.println(pos*i);
        }

        //4.Write a program to find the factorial value of any number entered through the keyboard.
        System.out.println("Q4");
            System.out.println("Enter Postive number");
            int factorial=s.nextInt();
            int total=1;
            for(int i=factorial;i>=1;i--){
                total=total*i;
            }
            System.out.println("The total  factorial is "+total);

        //5.Two numbers are entered through the keyboard. Write a program to find the value of one number raised to the power of another.
        System.out.println("Q5");
        System.out.println("Enter number one ");
        int num1=s.nextInt();
        System.out.println("Enter power number");
        int num2=s.nextInt();
       int resu=1;
       for(int i=1;i<=num2;i++){
           resu*=num1;
       }
       System.out.println("The result is "+resu);

       //6.Write a program that reads a set of integers, and then prints the sum of the even and odd integers.
        System.out.println("Q6");
       
        int even=0;
        int odd=0;
        while (true) {
            System.out.println("Run Y/N");
            s.nextLine();
            String ans = s.nextLine();
            if (ans.equalsIgnoreCase("y")) {
                System.out.println("Enter the number");
                int nx = s.nextInt();
                if (nx % 2 == 0) {
                    even += nx;
                } else {
                    odd += nx;
                }
            } else {
                break;
            }
        }

        System.out.println("The Number even is "+even +" And odd is "+odd);

        //7.Write a program that prompts the user to input a positive integer. It should then output a message indicating whether the number is a prime number.
        System.out.println("Q7");
        System.out.println("Enter Number Positive");
        int prom=s.nextInt();
          if(prom<0){
              System.out.println("the number is negative ");
          }
        boolean flag = false;
        for (int i = 2; i <= prom / 2; ++i) {
            // condition for nonprime number
            if (prom % i == 0) {
                flag = true;
                break;
            }
        }

        if (!flag)
            System.out.println(prom + " is a prime number.");
        else
            System.out.println(prom + " is not a prime number.");

        //8.Write a program to enter the numbers till the user wants and at the end it should display the count of positive, negative and zeros entered.
        System.out.println("Q8");
        int pos8=0;
        int nig=0;
        int zero=0;
        while (true){
            System.out.println("Run Y/N");
            s.nextLine();
            String ans=s.nextLine();
            if(ans.equalsIgnoreCase("y")){
                System.out.println("Enter the number");
                int nx=s.nextInt();
                if(nx>0){
                    pos8++;
                }
                else if (nx<0){
                    nig++;
                }
                else {
                    zero++;
                }
            }
            else{
                break;
            }
        }
        System.out.println("positve is "+pos8+" nigtive"+nig+" Zero "+zero);

        //9.Use a for loop to print headings for four weeks (Weeks 1 - 4). Then use another for loop to print the days (Days 1 -7) for each week.
        System.out.println("Q9");
        for (int i=1;i<=4;i++){
            System.out.println("Week "+i);
            for (int y=1;y<=7;y++){
                System.out.println("Day"+y);
            }

        }

        //10.Write a program thats check if the word is a palindrome or not. hint: A string is said to be a palindrome if it is the same if we start reading it from left to right or right to left.
        System.out.println("Q10");
        System.out.println("Enter the word");
        String wor=s.nextLine();
        String w="";
        for (int i=wor.length()-1;i>=0;i--){
            w+=wor.charAt(i);
        }

        if(wor.toLowerCase().equals(w.toLowerCase())){
            System.out.println("word is a palindrome");
        }
        else{
            System.out.println("word is not a palindrome");
        }

    }
