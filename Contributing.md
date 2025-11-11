♥️
Navigation Menu
ai-agents-intensive-2025-google-challenge

Code
Issues
Pull requests
ai-agents-intensive-2025-google-challenge
/CONTRIBUTING.md
ortall0201
ortall0201
4 days ago
119 lines (77 loc) · 2.79 KB

Preview

Code

Blame
Contributing Guidelines
This repository is a personal learning workspace for the 5-Day AI Agents Intensive course. However, if you would like to suggest improvements or share ideas, here is how to contribute.

Workflow
Adding Daily Notebooks
Complete the day notebook on Kaggle on the course platform
Download the notebook: File > Download .ipynb
Save to the correct folder: Place in the corresponding dayN_*/ directory
Update notes: Add key takeaways to notes.md in the same folder
Commit changes: Use atomic commits with clear messages
Example Commit Messages
Good commit messages are concise and descriptive:

Add Day 1 notebook: Agent basics
Update Day 2 notes: Multi-agent patterns
Fix typo in README
Add resources: Gemini API documentation
Git Best Practices
Atomic Commits
Make small, focused commits that represent a single logical change:

# Good: Separate commits for separate changes
git add day1_intro_to_agents/agent_basics.ipynb
git commit -m "Add Day 1 notebook: Agent basics"

git add day1_intro_to_agents/notes.md
git commit -m "Add Day 1 notes: Key takeaways"
Commit Frequency
Commit after completing each day notebook
Commit when adding significant notes or insights
Commit before making experimental changes
Security Rules
NEVER Commit:
API keys or tokens (GOOGLE_API_KEY, etc.)
.env files or environment configuration
kaggle.json credentials
Any file containing secrets or passwords
Always:
Use Kaggle Secrets for API keys in notebooks
Store local API keys in .env (already gitignored)
Review git diff before committing to catch accidental secrets
Use git log -p to review commit history if unsure
File Organization
Daily Folders
Each day folder should contain:

dayN_topic_name/
├── main_notebook.ipynb    # Downloaded from Kaggle
└── notes.md               # Personal takeaways and insights
Resources Folder
Keep all reference materials in resources/:

course_links.md: Official course URLs
kaggle_notes.md: Setup and API guides
Additional documentation as needed
Pull Requests (If Sharing)
If you are forking this repo and want to suggest improvements:

Fork the repository
Create a feature branch: git checkout -b feature/your-improvement
Make your changes
Test thoroughly
Submit a pull request with a clear description
Questions or Issues?
Check the Kaggle Discord for course support
Review resources/course_links.md for official resources
Open a GitHub issue for repo-specific questions
License
All contributions will be licensed under the MIT License. See LICENSE for details.

Happy learning!
