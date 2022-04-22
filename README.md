# Problem-01
//This is one of the projects where I have a hard time figuring out, I am a beginner at programming and would like to appreciate your help!
// The problem is: Create a program in Java that will read the CSV file and compute the Final Grade of the student using the computation below:
// Lab Exercise * 30% + Long Quiz * 30% + Alternative Assessment * 40% = Final Grade
//Then, display the final grade of each student.

import java.io.*;
public class ReadingFile {
    public static void main (String[]args){

        try{

            File myFile = new File("Grades.csv");
            BufferedReader br = new BufferedReader(new FileReader(myFile));
            String allLines = "";

            while((allLines = br.readLine()) != null){
                String row [] = allLines.split(",");
                double finalGrade = (Double.parseDouble(row[1])*.30) + (Double.parseDouble(row[2])*.30) + (Double.parseDouble(row[3])*.40);

            }

        }
        catch(IOException err){
            System.err.println("File not found.");
            
        }
}
}
