# Welcome to TrackPoint

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
## How to use
Copy the spreadsheet template, found [here](https://docs.google.com/spreadsheets/d/15hg__UhW7cKCcQLZcNwi6AsTuOdiSfdQcmO2ccb9sBs/edit?usp=sharing). Once copied and ready, do the following:
1. In the sheet _Epic_ fill out the values for `Title`, `Problem`, `Feature`, `Value`.
2. Navigate to the `Tasks` sheet and fill out your tasks. TaskID will automatically be filled out for you, when adding a title to a task.
3. Navigate to the `Users` sheet and declare your users. Like tasks, an ID will automatically be generated.

Now that you have filled out the sheet with your intended values, you need to configure your sheet and link it up with your GitHub repository.
This is done by doing the following:

4. Navigate to Github.com and create a new repository (repo).
5. Install [this](https://github.com/apps/trackpoint-github) Github app, to your newly created repo.
6. Navigate back to your Google spreadsheet and press `Share`, in the upper right-hand corner.
7. Under `General Access`, you want to set the sheet to `Anyone with the link` and define their right from `Viewer` to `Editor`.
8. Then you want to share the sheet, with the automated service account's mail, whose mail is:
```bash
trackpoint-backend-api@trackpointdb.iam.gserviceaccount.com
```
9. This account should have the role of `Editor`, in order to update your values in the sheet.
10. Fill out the cell values for `repoOwner` and `repoName`. (Hint: these values can be found in the URL for your Github repository)
```https://github.com/<repoOwner>/<repoName>```
11. Fill out the cell with the installationID you got when installing the Github app, 
12. Finally, install the add-on for Google sheet, called "Make for Google Sheet", if not already installed.
13. Navigate to the `Extension` tab within the Google sheet, click on Make for Google Sheet and go to settings.
14. Within the settings tab, within the text box called `Webhook URL` paste this link in.
```bash
https://trackpointapi-87527377987.europe-west1.run.app
```
Now whenever you make a new change to your tasks, the changes will be updated on your corresponding Github issues.

## For developers
Would you like to deploy this code yourself? Or make changes? Here's how you can set up the app within your environment.
FIrst and foremost, you need to have the right dependencies installed:

### **Dependencies:**
**Python:** The application is written in ```Python```. Please navigate to the offical [Python downloads page](https://www.python.org/downloads/). <br>
Ensure Python is correctly installed by running:

- `$ python -V` (should show "Python 3.x.x")
- `$ pip -V`

### **Docker**:
This project uses containerization with ```Docker```. Please install it from the [Docker downloads page](https://www.docker.com/products/docker-desktop/).

### **IDE**:
You must have an IDE that is comaptible with running devcontainers. We recommend [Visual Studio Code](https://code.visualstudio.com).

Now build the devcontainer and mount its resources.

