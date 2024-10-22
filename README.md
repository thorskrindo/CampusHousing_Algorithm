/** 
 * Author Thor Skrindo
 * Assignment: Campus Housing Priority Selection_Algorithm 
 * San Francisco State University; CSC101
 */

import java.util.Scanner;
public class HousingSelection {

    public static void main(String[] args) { 
        Scanner input = new Scanner(System.in); 
        
      System.out.println("Hi there and Welcome to the house selction app, we will ask a few questions to help determine your eligibility for campus housing");
         System.out.println("Press enter to begin");
        input.nextLine();
        System.out.print("How old are you?");

      // 2) Asking the user's academic year and providing point values for each year below
        int age = input.nextInt();
        System.out.println("What year are you in?");
         System.out.println("1: Freshman\n2: Sophomore\n3: Junior\n4: Senior\n5: Super Senior");

        System.out.print("Enter selcetion: ");
         int year = input.nextInt();

      // 3) Below we are asking if the user is on academic probation;(y or n) = Yes or no
        System.out.print("Are you on academic probation? (y or n) ");
         char academicProbation = input.next().charAt(0);

      // 4) Inquiring if the user is on diciplinary Probation;(y or n) = Yes or no
        System.out.print("Are you on diciplinary Probation? (y or n)");
         char diciplinaryProbation = input.next().charAt(0);

      //5) Asking if the user is on financial aid;(y or n) = Yes or no
        System.out.print("Are you on financial aid? (y or n) ");
        char financialAid = input.next().charAt(0);

      // 6) Asking the student about how many miles they live away from school, in order to assess if they are commuters or not
        System.out.print("How many miles do you live from school? Please estimate: ");
        int distance = input.nextInt();

      // 7) Asking if the student have had housing before;(y or n) = Yes or no
        int studentHousing = input.nextInt();
        System.out.print("Have you had housing before? (y or n)");
        char hadHousingBefore = input.next().charAt(0);

      // Now, we can to calculate the score based on the factors provided above with if-else statements
        int score = 0;

        if (age > 25) {

            score += 4;
        }else{ score += 0;


            if (age > 25) {
                score += 4;

        if (year >= 3 && year <= 5) {
            score += 3;
        }else{
            score += 0

            if (academicProbation == 'n') {

                score += 1;
                if (diciplinaryProbation == 'n') {
                score += 1;

                    if (financialAid == 'y') {
                    score += 2;

                        if (distance >= 50) {
                            score += 4;
                        }else{
                            score += 1;

                            if (hadHousingBefore == 'y') {
                                score += 1;
                            }else{
                                score +=1;

                        // Summarizing the users score
                        System.out.println("Thank you for your time, your determined score for husing is: " + score);
                        if (score >= 8) {
                            // Score above 8 = eligibility for housing
                            System.out.print("Congratulations, you are eligible for housing; ");

                            // Points summary resulting in lower than 8 equals no housing eligibility
                        } else {
                            System.out.print("Sorry, you are not eligible for housing at this point");
                          

                            input.close();
                        }
                    }

                }
            }
        }
    }
}




