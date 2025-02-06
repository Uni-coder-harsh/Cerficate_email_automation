# Certificate Generation and Emailing System

This project is designed to generate certificates for participants and send them via email. It uses a certificate template and a CSV file containing participant details to create personalized certificates and email them to the respective participants.

## Prerequisites

- Python 3.x
- Required Python packages (install using `pip install Pillow pandas`)

## Project Structure

- `CUK_temp.png`: Certificate template image.
- `students_data.csv`: CSV file containing participant details (name and email).
- `generated_certificates/`: Folder where generated certificates will be saved.
- `certificate_generator.py`: Main script to generate and email certificates.

## Usage

1. **Install Required Packages:**

    ```bash
    pip install Pillow pandas
    ```

2. **Prepare CSV File:**

    Ensure your CSV file (`students_data.csv`) has the following columns:
    - `name`: Participant's name
    - `email`: Participant's email address

3. **Run the Script:**

    Execute the script to generate and email certificates:

    ```bash
    python certificate_generator.py
    ```

## Functions

- `create_certificate(template_path, output_folder, name, email)`: Generates a certificate for a single participant.
- `send_email(recipient, subject, body, attachment_path)`: Sends an email with the certificate attached.
- `process_certificates(template_path, csv_path, output_folder)`: Processes the CSV file to generate and email certificates for all participants.

## Logging

The script uses logging to provide information about the process. Logs include information about certificate creation and email sending status.

## License

This project is licensed under Harsh. Please see the LICENSE file for more details.