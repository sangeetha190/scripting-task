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
