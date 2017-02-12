# Add created at and updated at column to existing table
    ALTER TABLE `tableName` 
    ADD COLUMN  createdAt TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    ADD COLUMN  updatedAt TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP

# Get random numberOfRows 
    SELECT * FROM `tableName` ORDER BY RAND() LIMIT `numberOfRows`

