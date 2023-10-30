# 2023 Fall Learning Analytics Hackathon
Welcome to the #hack-la-2023 github repository.

Please register for the hackathon if you haven't ready done so: https://events.ctlt.ubc.ca/events/2023-fall-learning-analytics-hackathon/

## 📅 Schedule
### Saturday Nov 4th
* 9:00am - Start hacking! (Coffee and light refreshments provided)
* 12ish Lunch (provided)
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
* [clean data](https://www.sisense.com/glossary/data-cleaning/)
* contribute to [open source projects](https://docs.github.com/en/get-started/quickstart/contributing-to-projects) (like this hackathon!)
* apply data analytics and programming skills
* work in a team
* build cool stuff!

## 🤔 Ask For Help
Please ask the volunteers and your peers for help. We're all here to learn together!

## ⚙️ Getting Started
These instructions will get you a copy of the project up and running on your local machine for use with your own Canvas API tokens.

- TODO: add link to quiz to request Canvas events data and add this data to the data folder
- review [data_dictionary](./data_dictionary.md)
- TODO: add git commit hook to clear notebook contents

### Prerequisites
1. **Install [Git](https://git-scm.com/downloads)**.
1. **Install [Python](https://www.python.org/)** (if you want to use our [starter kit](./starter_kit/starter.ipynb)).
1. **Install [Jupyter notebooks](https://jupyter.org/install)** (if you want to use our [starter kit](./starter_kit/starter.ipynb)).
1. **Install [Visual Studio Code](https://code.visualstudio.com/)** (optional but recommended).

### Cloning and setup
1. Fork this repo.
![fork](./_imgs/fork.png)
1. Copy clone link.
![clone](./_imgs/clone.png)
1. Open terminal on Mac or command line on Windows. We like to use [VSCode's integrated terminal](https://code.visualstudio.com/docs/editor/integrated-terminal), as it works for both Mac and PC.
1. Clone repo. `git clone {paste URL you copied}`
1. Navigate into repo. `cd hack-la-203`
1. Rename the `src_rename_me` folder with your group name. All of your work should be contained inside this folder to reduce the likelihood of merge conflicts when you submit your work later. 
1. Download your events data from the Canvas quiz and place under the `data` folder. Anything that is contained in this folder is gitignored. 
1. [Optional] Run the `starter.ipynb`file.
1. Start hacking!

### Final Submission
1. Update the `final_submission_template.md` that is inside your group's folder. 
1. Create a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) from your forked repo to the [original repo](https://github.com/UBC-LA-Hackathon/hack-la-2023).
1. Your pull request will be merged after it is reviewed.  

## Additional resources:
- [Guide for using the Canvas API](https://learninganalytics.ubc.ca/for-students/canvas-api/)
- [Python Canvas API Starter Kit](https://github.com/ubc/getting-started-with-the-canvas-api-with-python)
- [NodeJS Canvas API Starter Kit](https://github.com/ubc/getting-started-with-the-canvas-api-with-node)
- [Canvas API Documentation](https://canvas.instructure.com/doc/api/)