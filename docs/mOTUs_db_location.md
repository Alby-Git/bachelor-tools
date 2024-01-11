# Location of the mOTUs Database

The setup script for the mOTUs tool saves the mOTUs database in the same directory where it is executed. Here's the process explained in a simple form:

## 1. Determining the Script Execution Location

```python
path_mOTUs = os.path.realpath(__file__)
path_array = path_mOTUs.split("/")
relative_path = "/".join(path_array[0:-1]) + "/"
```

- `__file__`: The absolute path of the script file.
- `relative_path`: The path of the directory where the script is located.

## 2. Downloading and Temporarily Storing the Database

```python
db_name = relative_path + "db_mOTU.tar.gz"
```

- The database is downloaded as a `.tar.gz` file and temporarily stored under `db_name` in the script's execution directory.

## 3. Extracting and Final Storing

```python
extract_cmd = "tar -zxvf " + db_name + " -C " + relative_path
```

- The downloaded file is extracted in the `relative_path` directory.

**Summary**: The mOTUs database is saved and unpacked in the directory where the setup script is executed. The exact path depends on the location of script execution on the user's system.