package StudentGradeTracker;
import java. util. Arraylist;
import java. util. Scanner;
 class StudentGradeTracker {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner scanner = new Scanner(System.in);
		ArrayList<Double> grades = new ArrayList<>();
		System.out.println("Enter the number of students:");
		int numberofstudents = scanner.nextInt();
		for(int i = 0; i < numberofstudents;i++){
		System.out.println("Enter the grade for student" + (i + 1) + ":");
		double grade=scanner.nextDouble();
		grades.add(grade);
		}
		double sum = 0;
		double highest = grades.get(0);
		double lowest = grades.get(0);
		for(double grade : grades) {
			sum += grade;
			if(grade>highest) {
				highest = grade;
				}
			if(grade<lowest) {
				lowest = grade;
			    }
		     }
		double average = sum /grades.size();
		System.out.printf("Average grade: %.2f%n", average);
		System.out.printf("Highest grade: %.2f%n", highest);
		System.out.printf("Lowest grade: %.2f%n", lowest);
		scanner.closer();
	}
		

}
