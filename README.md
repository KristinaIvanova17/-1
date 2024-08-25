import java.util.Base64;

public class Main
{
  public static String encodeCredentialsToBase64(String email, String code) {
        String credentials = email + ":" + code;
        String encodedCredentials = Base64.getEncoder().encodeToString(credentials.getBytes());
        return encodedCredentials;
    }

    public static void main(String[] args) {
        String email = "example@example.com";
        String code = "password123";
        String encodedCredentials = encodeCredentialsToBase64(email, code);
        System.out.println(encodedCredentials);
    }
}
