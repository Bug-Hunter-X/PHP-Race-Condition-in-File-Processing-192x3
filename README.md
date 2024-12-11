# PHP File Processing Race Condition

This repository demonstrates a race condition in a PHP function designed to process and write data to a file.  The `processFile()` function attempts to use `flock()` for file locking, but this isn't robust enough to handle concurrent requests that might arrive while the file is being written.  This can result in data corruption or loss.

The `bug.php` file contains the flawed code.  The `bugSolution.php` file provides a corrected version that uses a more reliable locking mechanism to prevent race conditions.