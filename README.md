[![Codacy Badge](https://api.codacy.com/project/badge/Grade/8897d8dd8121474e863127f0fe9a2810)](https://app.codacy.com/gh/VureZ/test?utm_source=github.com&utm_medium=referral&utm_content=VureZ/test&utm_campaign=Badge_Grade)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/dbfb76df49e2493a9cea3f95f5be863e)](https://app.codacy.com/gh/VureZ/test/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade)

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Введите первое число:");
        short num1 = scanner.nextShort();

        System.out.println("Введите второе число:");
        short num2 = scanner.nextShort();

        short diff = (short) (num1 - num2);
        System.out.println("Разность: " + diff);

        short result = (short) (~(num1 | num2));
        System.out.println("Результат битовых операций: " + result);
    }
}
