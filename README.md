# OWNEROUS
## Bulk change Google Drive ownership, the ownerous way...

Either download the binary from the Releases page, or build your own like this:

    env GOOS=darwin GOARCH=amd64 go build -o ownerous .
    env GOOS=windows GOARCH=amd64 go build -o ownerous.exe .

### Instructions

1) Get your `credentials.json` from the Google Cloud Console page as described [here](https://developers.google.com/drive/api/v3/quickstart/python) and put them besides the executable. 

2) Run the executable with one argument: The email address of the new owner of whichever file you own that has been shared. This won't change anything with your private files, it will only change ownership if the file was already shared and you happened to be the owner. 

### Example:

$ ./ownerous john.smith@gmail.com

So now, John Smith is the new owner of all the documents I have shared in the past. Good for him! 
