# IIS LogParser

This project is a Windows application that allows users to view and filter IIS logs. It includes features like time zone conversion for IIS log timestamps and SQL-like query functionality for filtering log data and export the result.

## Features

- **View IIS Logs**: Load and display IIS logs in a structured format within a grid.
- **Time Zone Conversion**: Convert the date and time in the logs to the local server time or any selected time zone.
- **Basic SQL Query Support**: Filter and query the log data using basic SQL-like syntax (similar to LogParser.exe).
- **Export Logs**: Export filtered or unfiltered log data back into the original IIS log format.
- **Responsive UI**: The grid and query input fields resize with the form window.

## Installation

1. Clone the repository or download application:
   ```bash
   https://github.com/hridaydutta/LogParser.git
   ```
   
2. Double click the IISLogParser.exe to use it.

3. .Net Core 8.0 or above is required run the application.

## Usage

1. Launch the application and use the **File -> Open** menu button to select an IIS log file.
2. The logs will be displayed in the grid format.
3. Use the **Time Zone** dropdown to select the appropriate time zone for log conversion.
4. Enter SQL-like queries in the query text box to filter log data. For example:
   ```sql
   SELECT [date], [time], [cs-method], [cs-uri-stem] WHERE [time-taken] > 200
   ```
   ```WHERE <tablename>``` is not required.
5. Click the **Execute Query** button to filter the data.
6. Use the **File -> Export** menu button to save the filtered logs.

## Example Queries

- **Filter by status code**:
   ```sql
   SELECT * WHERE [sc-status] = 500
   ```
- **Select specific columns**:
   ```sql
   SELECT [date], [time], [cs-method], [sc-status] 
   ```
- **Filter by date**:
   ```sql
   SELECT * WHERE [date] = '2024-10-06'
   ```

## License

This project is licensed under the **Use-Only License**. You are free to use the software, but modification, distribution, or selling is prohibited. See the [LICENSE](LICENSE) file for more details.

## Contributing

If you find any bugs or have suggestions for improvements, feel free to open an issue or submit a pull request.

## Contact

For any inquiries, please contact **Hriday Ranjan Dutta**.

---

**Disclaimer**: This utility is provided "as is", without any warranty of any kind.
```
