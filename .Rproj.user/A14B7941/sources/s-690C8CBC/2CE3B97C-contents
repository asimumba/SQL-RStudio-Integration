#Connection options to SQL Server databases

con <- DBI::dbConnect(odbc::odbc(),
                      Driver    = "SQL Server",
                      Server    = "AARON-SIMUMBA\\SQLEXPRESS",
                      Database  = "AdventureWorks2017",
                      Port      = 1433,
                      UID       = "rstudioconnect",
                      PWD       = .rs.askForSecret(name ="AARON-SIMUMBA\\SQLEXPRESS",
                                                   title = "Enter Password",
                                                   prompt = "Database Password:"))

con <- DBI::dbConnect(odbc::odbc(),
                      Driver    = "SQL Server",
                      Server    = "AARON-SIMUMBA\\SQLEXPRESS",
                      Database  = "AdventureWorks2017",
                      Port      = 1433,
                      UID    = rstudioapi::askForPassword("Database user"),
                      PWD    = rstudioapi::askForPassword("Database password"))


library(RODBC)

conn <- RODBC::odbcDriverConnect('driver={SQL Server};
                                server=AARON-SIMUMBA\\SQLEXPRESS;
                                database=AdventureWorks2017;
                                trusted_connection=true')

data <- sqlQuery(conn, "SELECT * FROM Production.TransactionHistoryArchive;")

