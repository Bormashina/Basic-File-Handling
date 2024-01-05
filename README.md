# Basic-File-Handling
Java Code for Basic File Handling
import java.io.File;
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class FileHandling {
    public static void main(String[] args) throws IOException {
        // Writing to a file
        FileWriter writer = new FileWriter("example.txt");
        writer.write("Hello, File Handling!");
        writer.close();

        // Reading from a file
        File file = new File("example.txt");
        Scanner scanner = new Scanner(file);
        while (scanner.hasNextLine()) {
            System.out.println(scanner.nextLine());
        }
        scanner.close();
    }
}
