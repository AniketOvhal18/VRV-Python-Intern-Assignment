# VRV-Python-Intern-Assignment
This Python script is designed to analyze log files, extract key information, and generate useful insights. It demonstrates core programming skills essential for cybersecurity-related tasks, including file handling, string manipulation, and data analysis

## Features

1. **Request Count by IP Address**
   - Parses the log file to extract IP addresses.
   - Calculates the number of requests made by each IP.
   - Displays results in descending order of request counts.

   **Example Output:**
   ```
   IP Address           Request Count
   192.168.1.1          234
   203.0.113.5          187
   10.0.0.2             92
   ```

2. **Most Frequently Accessed Endpoint**
   - Extracts resource paths (endpoints) from the log file.
   - Identifies the most accessed endpoint and its access count.

   **Example Output:**
   ```
   Most Frequently Accessed Endpoint:
   /home (Accessed 403 times)
   ```

3. **Suspicious Activity Detection**
   - Detects brute-force login attempts based on failed login entries (e.g., HTTP status code `401`).
   - Flags IP addresses with failed login attempts exceeding a configurable threshold (default: 10 attempts).

   **Example Output:**
   ```
   Suspicious Activity Detected:
   IP Address           Failed Login Attempts
   192.168.1.100        56
   203.0.113.34         12
   ```

4. **Output Results**
   - Displays results in the terminal in a structured format.
   - Saves results to a CSV file named `log_analysis_results.csv` with the following structure:

     - **Requests per IP:**
       Columns: IP Address, Request Count

     - **Most Accessed Endpoint:**
       Columns: Endpoint, Access Count

     - **Suspicious Activity:**
       Columns: IP Address, Failed Login Count

## Project Structure

```
project-folder/
├── log_analysis.py        # Main script file
├── sample.log            # Sample log file (input)
├── log_analysis_results.csv # CSV file with analysis results (output)
├── README.md              # Documentation file
```

## Code

The complete implementation of the log analysis is available in the https://github.com/AniketOvhal18/VRV-Python-Intern-Assignment/blob/main/vrv%20assignment.ipynb file.

## How to Run the Script

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/AniketOvhal18/log-analysis.git
   ```

2. Navigate to the project directory:
   ```bash
   cd log-analysis
   ```

3. Ensure Python is installed (version 3.6 or higher).

4. Run the script using the command:
   ```bash
   python log_analysis.py
   ```

5. View the results in the terminal and check the generated `log_analysis_results.csv` file for a detailed report.

## Requirements

- Python 3.6+
- Libraries:
  - `re`
  - `csv`
  - `collections`

No external dependencies are required.

## Sample Input Log File

An example `sample.log` is included with the project. Here are some sample entries:
```
192.168.1.1 - - [03/Dec/2024:10:12:34 +0000] "GET /home HTTP/1.1" 200 512
203.0.113.5 - - [03/Dec/2024:10:12:35 +0000] "POST /login HTTP/1.1" 401 128 "Invalid credentials"
10.0.0.2 - - [03/Dec/2024:10:12:36 +0000] "GET /about HTTP/1.1" 200 256
```

## Output Results

### Terminal Output:

**Requests Per IP Address:**
```
IP Address           Request Count
192.168.1.1          5
203.0.113.5          8
10.0.0.2             3
```

**Most Frequently Accessed Endpoint:**
```
/home (Accessed 403 times)
```

**Suspicious Activity Detected:**
```
IP Address           Failed Login Attempts
192.168.1.100        56
203.0.113.34         12
```

### CSV Output:

A `log_analysis_results.csv` file is generated with three sections:

1. Requests per IP:
   ```csv
   IP Address,Request Count
   192.168.1.1,5
   203.0.113.5,8
   10.0.0.2,3
   ```

2. Most Accessed Endpoint:
   ```csv
   Endpoint,Access Count
   /home,403
   ```

3. Suspicious Activity:
   ```csv
   IP Address,Failed Login Count
   192.168.1.100,56
   203.0.113.34,12
   ```

## Evaluation Criteria

- **Functionality:**
  - Correct processing of log file data.
  - Fulfillment of all requirements: IP request counts, most accessed endpoint, and suspicious activity detection.

- **Code Quality:**
  - Clear, modular, and well-commented code.
  - Meaningful variable names and adherence to Python best practices.

- **Performance:**
  - Efficient handling of the provided log file.
  - Scalable to larger files without significant performance degradation.

- **Output:**
  - Accurate and formatted output in both terminal and CSV.

## Author
Your Aniket Prabhakar Ovhal
Email: aniket.ovahl@dypic.in  
GitHub:https://github.com/AniketOvhal18

