# 2023 Fall Learning Analytics Hackathon
Welcome to the #hack-la-2023 github repository.

Please **[register](https://events.ctlt.ubc.ca/events/2023-fall-learning-analytics-hackathon/)** for the hackathon if you haven't ready done so.

## 📅 Schedule
### Saturday Nov 4th
* 9:00am - Start hacking! (Coffee and light refreshments provided)
* 12ish Lunch (provided)
* 2pm Check-In (maybe! look out for Canvas announcement!)
* 5ish Dinner (provided)
* 6ish Presentations Start
* 8ish End of Hackathon!

## 🔨 What You'll Build
[Tuum Est](http://100.ubc.ca/timeline/the-ubc-motto-and-crest-are-created/)

## 📚 What You'll Learn
By participating in this hackathon, you'll learn to:

* use the [Canvas API](https://canvas.instructure.com/doc/api/)
* use the [Canvas Live Events data](https://canvas.instructure.com/doc/api/file.data_service_introduction.html)
* explore the data that [Canvas collects from you](https://learninganalytics.ubc.ca/ethics-policy/students-learning-analytics-and-privacy/)
* contribute to [open source projects](https://docs.github.com/en/get-started/quickstart/contributing-to-projects) (like this hackathon!)
* apply data analytics and programming skills
* work in a team
* build cool stuff!

## 🤔 Ask For Help
Please ask the volunteers and your peers for help. We're all here to learn together!

## ⚙️ Getting Started
### Prerequisites
1. **Install [Git](https://git-scm.com/downloads)**.
1. **Install [Python](https://www.python.org/)** (if you want to use our [starter kit](./rename_me/starter.ipynb)).
1. **Install [Jupyter notebooks](https://jupyter.org/install)** (if you want to use our [starter kit](./rename_me/starter.ipynb)).
1. **Install [Visual Studio Code](https://code.visualstudio.com/)** (optional but recommended).

### Cloning and setup
1. Fork this repo.
![fork](./_imgs/fork.png)
1. Copy clone link.
![clone](./_imgs/clone.png)
1. Open terminal on Mac or command line on Windows. We like to use [VSCode's integrated terminal](https://code.visualstudio.com/docs/editor/integrated-terminal), as it works for both Mac and PC.
1. Clone repo. `git clone {paste URL you copied}`
1. Navigate into repo. `cd hack-la-2023`
1. Rename the `rename_me` folder with your group name. All of your work should be contained inside this folder to reduce the likelihood of merge conflicts when you submit your work later. 
1. Download your events data from the Canvas quiz and place under the `{group_name}/data` folder, and rename the file as `events.csv`. Anything that is contained in this folder is gitignored.
1. [Optional] Run the `starter.ipynb`file.
1. Start hacking!

### Git and Jupyter ⚠️
1. Note that if you're using Jupyter Notebooks, the output cells that contain potentially sensitive data are saved and can accidentally be added, committed, and pushed to Github. Please take care to **clear your cells** before adding and committing your Notebooks. 
1. VSCode has the ability to [clear all outputs](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_clear-output-or-restartinterrupt-the-kernel) in a Jupyter notebook.

### Final Submission
1. Update the `final_submission_template.md` that is inside your group's folder. 
1. Create a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) from your forked repo to the [original repo](https://github.com/UBC-LA-Hackathon/hack-la-2023).
1. Your pull request will be merged after it is reviewed.  

## Additional resources:
- [Guide for using the Canvas API](https://learninganalytics.ubc.ca/for-students/canvas-api/)
- [Python Canvas API Starter Kit](https://github.com/ubc/getting-started-with-the-canvas-api-with-python)
- [NodeJS Canvas API Starter Kit](https://github.com/ubc/getting-started-with-the-canvas-api-with-node)
- [Canvas API Documentation](https://canvas.instructure.com/doc/api/)
- [Canvas API Live](https://canvas.ubc.ca/doc/api/live#!/)
