 /*
    name : Maharshi Bhatt
    date : 20/03/2024
    aim  : Reverse the String using Stack functions(Push & pop).
 */
import java.util.*;

class StringRev {
    static int top = -1;
    String a[];

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        StringRev sr = new StringRev();
        System.out.print("\u001b[33mEnter the string: \u001b[0m");
        String str = sc.nextLine();
        sr.a = new String[str.length()];
        String []chstr = str.split("");
        String rev = sr.reverse(chstr);
        System.out.println(rev);
    }

    String reverse(String [] s) {
        String rev = "";
        for (int i = 0; i < s.length; i++) {
            push(s[i]);
        }
        for (int i = 0; i < s.length; i++) {
            rev += pop();
        }
        return rev;
    }

    void push(String s) {
        top++;
        a[top] = s;
    }

    String pop() {
        top--;
        return a[top + 1];
    }
}
