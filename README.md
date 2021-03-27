import java.util.Scanner;
public class TestAvgAndGrade {
public static void main(String[] args) {
Scanner kb = new Scanner(System.in);
char letterGrade = 'A';

System.out.print("Enter test grade for student 1:");
double score1 = kb.nextDouble();
System.out.print(" Enter test grade for student 2:");
double score2 = kb.nextDouble();
System.out.print(" Enter test grade for student 3:");
double score3 = kb.nextDouble();
System.out.print(" Enter test grade for student 4:");
double score4 = kb.nextDouble();
System.out.print(" Enter test grade for student 5:");
double score5 = kb.nextDouble();

System.out.print(" The letter grades are as follows:\n");
System.out.println("Student 1: "+ determineGrade(score1));
System.out.println("Student 2: "+ determineGrade(score2));
System.out.println("Student 3: "+ determineGrade(score3));
System.out.println("Student 4: "+ determineGrade(score4));
System.out.println("Student 5: "+ determineGrade(score5));

double average = calcAverage(score1,score2,score3,score4,score5);
System.out.printf("The average grade was: %.2f\n",average);
}
public static char determineGrade(double score){
char grade;
if(score <60)
grade = 'F';
else if(score <70)
grade = 'D';
else if(score <80)
grade ='C';
else if(score <90)
grade = 'B';
else
grade ='A';

return grade;
}

public static double calcAverage(double sc1,double sc2,double sc3, double sc4,double sc5){
double av = (double)(sc1+sc2+sc3+sc4+sc5)/5;
return av;
}


}
