# Port Scanner

## Project Overview

This project is a **basic network port scanner** written in Python. It allows users to scan multiple IP addresses for open ports within a specified range. A port scanner is a tool commonly used in network security for identifying open and potentially vulnerable ports on a device. This project serves as a foundational tool for exploring network security, making it a valuable addition for anyone interested in ethical hacking or cybersecurity.

## Features

- **Single or Multiple Target Scanning**: Users can enter a single IP address or multiple IP addresses separated by commas.
- **Port Range Customization**: Allows users to specify how many ports to scan, starting from port 1 up to the desired port number.
- **Open Port Detection**: Identifies and displays open ports for each specified IP address.
- **Colored Output**: Uses color-coded messages for better readability when scanning multiple targets.

## How It Works

1. **User Input**: The program prompts the user to input the target IP addresses and the number of ports to scan.
2. **Target Parsing**: If multiple targets are specified, the program separates them and scans each IP individually.
3. **Port Scanning**:
   - For each IP address, the program iterates through the specified range of ports (from 1 up to the given limit).
   - It attempts to connect to each port on the IP address.
   - If a connection is successful, it indicates that the port is open. If the connection fails, it moves to the next port.
   
## Technologies Used

- **Python**: The main programming language for this project.
- **Socket Library**: Used to create network connections and check if ports are open.
- **Termcolor Library**: Provides color-coded text output to enhance readability in the terminal.

## Project Structure

- **`scan(target, ports)`**: The main function for scanning a single target IP over a range of ports.
- **`scan_port(ipaddress, port)`**: Attempts to connect to a specified port on a given IP address, printing open ports.
- **User Input Handling**: Processes user input for target IPs and port range, supports multiple IPs.

## Getting Started

### Prerequisites

- **Python 3.x**
- Install the `termcolor` library:
  ```bash
  pip install termcolor
  ```

### Running the Project

1. Clone the repository or download the script.
2. Open a terminal in the project directory.
3. Run the script:
   ```bash
   python portscanner.py
   ```
4. Follow the prompts to enter IP addresses and specify the range of ports to scan.

### Example Usage

```plaintext
[*] Enter Targets To Scan (split them by ,): 192.168.1.1,192.168.1.2
[*] Enter How Many Ports You Want To Scan: 100
```

This example would scan the first 100 ports on both `192.168.1.1` and `192.168.1.2`.

## Project Goals

This project was developed to:
- Gain hands-on experience with network programming in Python.
- Understand socket programming and its role in port scanning.
- Explore basic network security concepts, particularly in identifying open ports on devices.

## Limitations and Future Improvements

- **Service Detection**: Currently, this tool only identifies if a port is open, without providing information about the service running on the port.
- **Port Range Flexibility**: Enhancing the tool to specify custom port ranges (e.g., 20-100) would add flexibility.
- **Error Handling**: Adding more detailed error handling to provide feedback if the script encounters issues (e.g., network permissions, IP connectivity).

## Disclaimer

This tool is intended for educational and ethical purposes only. Scanning a network or system without permission is illegal and unethical. Always ensure you have authorization before using this tool to scan any network or device.

## License

This project is open-source and available under the MIT License.
