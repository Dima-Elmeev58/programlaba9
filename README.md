# programlaba9
import java.util.Scanner;
public class Main {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Введите Факультет:");
        String fakultet = input.nextLine();
        System.out.println("Введите дату постулпения:");
        String data_postupil = input.nextLine();
        Student[] massiv = new Student[3];
        massiv[0] = new Student("Elmeev.D.S", "2023.09.01", "Street1", 79042661461L, 1, "Инф-Тех");
        massiv[1] = new Student("Lifanov.S.I", "2023.09.01", "Street2", 79042634461L, 1, "Инф-Тех");
        massiv[2] = new Student("Rosanov.A.K", "2023.09.01", "Street3", 79022661461L, 1, "Инф-Тех");
        for (int i = 0; i < massiv.length; i++) {
            System.out.println(massiv[i].getFIO());
            if (massiv[i].getFakultet().equals(fakultet)) {
                System.out.println("Студент " + massiv[i].getFIO() + " учится на заданном вами факультете.");
            }
            if (massiv[i].getData_postup().equals(data_postupil)) {
                System.out.println("Студент " + massiv[i].getFIO() + " поступивший в заданном вами году.");
            }
        }
    }

    static class Student {
        private String FIO;
        private String Data_postup;
        private String Adress;
        private long Phone;
        private int kurs;
        private String fakultet;

        public Student(String FIO, String Data_postup, String Adress, long Phone, int kurs, String fakultet) {
            this.FIO = FIO;
            this.Data_postup = Data_postup;
            this.Adress = Adress;
            this.Phone = Phone;
            this.kurs = kurs;
            this.fakultet = fakultet;
        }

        public void setFIO(String FIO) {
            this.FIO = FIO;
        }

        public String getFIO() {
            return this.FIO;
        }

        public String getData_postup() {
            return this.Data_postup;
        }

        public String getAdress() {
            return this.Adress;
        }

        public void setPhone(long phone) {
            this.Phone = phone;
        }

        public long getPhone() {
            return this.Phone;
        }

        public void setKurs(int kurs) {
            this.kurs = kurs;
        }

        public String getFakultet() {
            return this.fakultet;
        }
    }
}
