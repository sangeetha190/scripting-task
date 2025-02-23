# scripting-task
1. Create a shell script to print the HTTP error code of guvi.in & print, the success/failure message based on the error code response
   - HTTP_STATUS=$(curl -o /dev/null -s -w "%{http_code}" "$URL")
      - curl is a command-line tool used to send HTTP requests.
      - -o /dev/null          => Discards the output (we don’t need the webpage content)
      - -s                    => 	Runs curl in silent mode (hides progress output)
      - -w "%{http_code}"     => Extracts only the HTTP status code


- Status Code	Meaning
  - 200 ✅	Success (Website is reachable)
  - 301/302 🔄	Redirect (URL is moved)
  - 403 ❌	Forbidden (Access denied)
  - 404 ❌	Not Found (Wrong URL)
  - 500+ ⚠️	Server Error (Website is down)
![image](https://github.com/user-attachments/assets/f75e53d7-ee32-49e0-9c3b-ec28c843bb61)

2. Given a file, replace all occurrence of the word "give" with "learning" from 5th line till the end in only those lines that contain the word "welcome"

- The sed Command:
- sed -i
    - The -i option modifies the file in place without needing redirection (>).
-'5,$'
    - 5,$ specifies the range → It starts from line 5 and goes to the end of the file ($).
- {/Welcome/s/give/learning/g}
   - /Welcome/ → This means only modify lines that contain "Welcome" (case-sensitive).
- s/give/learning/g → This is the substitution command:
   - s/old/new/g → Replaces "give" with "learning".
   - The g at the end ensures all occurrences in a line are replaced
- ## Before 
![Screenshot 2025-02-23 235348](https://github.com/user-attachments/assets/147fc9e2-c836-47a8-bc4e-3da7f361743c)

- ## After command executed
![image](https://github.com/user-attachments/assets/cf16c4c6-86c0-40f5-a542-fe6814e9bff1)
![image](https://github.com/user-attachments/assets/0184a1c1-7dc6-4afa-bc7e-95dc6bfcb403)
