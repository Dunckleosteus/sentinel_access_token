# Use
The goal is to create a `nushell` script to automatically create or update the the ==access token== needed to download data from [Copernicus](https://documentation.dataspace.copernicus.eu/Registration.html) api. 

# How to use
- You need to have nushell installe
- It should work on linux and windows, I have not tested it on mac
- Make sure it is allowed to be executed (use chmod on linux)

Run the script from the command line by typing `./access_token`. The first time it runs it will ask for your email and password used you use to log into Copernicus. This data is not saved and is only needed when the refresh key and access key are out of date.
> When running the script later it should not ask for it as long it has not gone out of date, the refresh key goes out of date in an hour.

## Security
To limit the amount of times the email and password are used, the script used the refresh key where possible.

## Output
The program will ouput a access token if the user information is correct. This can then be assigned to a variable.

# TODO
- [ ] Error handling
- [ ] Adding flags like --help
- [ ] Testing on other platforms
