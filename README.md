# 2025-05-01-mcp-hacks
https://lu.ma/msft-hack-night-05-01-2025

## Steps

1. Download and install Docker Desktop for Mac from https://www.docker.com/products/docker-desktop
2. Pull the SQL Server image by running: `docker pull mcr.microsoft.com/mssql/server:2022-latest`
3. Run the SQL Server container: `docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=YourStrong@Passw0rd" -p 1433:1433 --name sql1 -d mcr.microsoft.com/mssql/server:2022-latest`
   - Instructions sourced from [How to Install SQL Server on MacOS?](https://www.geeksforgeeks.org/how-to-install-sql-server-on-macos/)
   - Validate that the container is running with: `docker container ps`
4. Install the SQL Server command-line tools if not already installed: `brew install sqlcmd`
5. Connect to the SQL Server container: `sqlcmd -S localhost -U sa -P YourStrong@Passw0rd`
   - Validate the connection by running: `SELECT 1; GO`

---

*This README was written with the assistance of AI*
