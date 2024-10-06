- If K is larger than or equal to size of both strings, then definitely it is possible
- when k is smaller, we first calculate the required number of moves.
	- moves > k -> then not possible
	- moves = k -> possible
	- moves < k -> then it depends of k-moves is even (possible) or odd (not). 

```Java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;

class Result {

    /*
     * Complete the 'appendAndDelete' function below.
     *
     * The function is expected to return a STRING.
     * The function accepts following parameters:
     *  1. STRING s
     *  2. STRING t
     *  3. INTEGER k
     */

    public static String appendAndDelete(String s, String t, int k) {
        int m= s.length();
        int n= t.length();
        if(k>=(m+n)) return "Yes";
        int i = 0;
        for(i=0;i<Math.min(m,n);i++){
            if(s.charAt(i)!=t.charAt(i)){
                break;
            }
        }
        int moves = m+n-2*i;
        return (k<moves)||(k-moves)%2!=0?"No":"Yes";
    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        String s = bufferedReader.readLine();

        String t = bufferedReader.readLine();

        int k = Integer.parseInt(bufferedReader.readLine().trim());

        String result = Result.appendAndDelete(s, t, k);

        bufferedWriter.write(result);
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}

```