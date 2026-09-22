
# OVERVIEW

In this guide you will learn how to use python's requests library to
fetch user data from a public web API and display the result in the
terminal.integrating external data programmatically allows your
applications to consume real time information-such as weather
updates,stocks,market figures,or user profile metadata.

# PREREQUISITIES

Before starting,ensure that you have the following setup on your system:

1.  Python 3.8 or higher installed.

2.  pip (Python package installer) configured.

3.  request library (installation covered in step 1).

4.  Basic familiarity with the command prompt (windows) or terminal
    (macOS/linux).

# PROCEDURE

1.  Open the command prompt(windows) or terminal (macOSl/inux)

2.  Run the folllowing command to install the required HTTP library:

    ``` {.bash language="bash"}
    pip install requests
    ```

    NOTE : If you are using visual studio code or another IDE,you can
    run this command directly in the built-in-terminal.

    ## step 2 : Create and write the python script

3.  Open your code editor or terminal and create a new file named.

                fetch_user.py

4.  Paste the following python code into

          fetch user.py.  

            import requests

        # Send a GET request to the GitHub API
        response = requests.get("https://api.github.com/users/octocat")

        # Parse the JSON response body
        data = response.json()

        # Print specific details from the response
        print(f"User: {data['login']}")
        print(f"Name: {data['name']}")
        print(f"Public Repos: {data['public_repos']}")

5.  save the file.

    ## step 3: Run the script

6.  In the terminal,navigate to the folder where

            fetch_user.py

    is saved.

7.  Execute the script using python:

            python fetch_user.py

    NOTE:Depending on how python installed on your system,you may need
    to use

            python3 fetch_user.py

# VERIFICATION

To confirm that your api request was successful,examine your terminal
output. you should see the following details printed on your screen.

    User: octocat
    Name: The Octocat
    Public Repos: 8

1.  Success: Receiving the formatted profile text confirms your script
    successfully queried the GitHub API and parsed the JSON payload.

2.  Troubleshooting: If you receive a

                ModuleNotFoundError: No module named 'requests

    re-run step 1 to verify the package installation.
