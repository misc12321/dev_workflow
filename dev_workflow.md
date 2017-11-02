## Developer Gets Assigned Ticket
*   Image of Jira ticket:
*   Review and clarify the ticket requirements 

## Developer Creates Branch For Ticket
*   From the 'initial_launch' or freshest possible branch, create new branch for the specific ticket using the ticket ID as branch name. (i.e PS-1). 
*   `git checkout -b PS-1` or whichever number the ticket is*
*   Once branch is created, Jira will be triggered to set status from `To Do` to `In Progress`

## Developer Works on Ticket
*   Make sure to follow all guidelines for the project directory structure and best coding practices
*   Good commit practices include frequent commits tied to one task completed to help track changes throughout branch
*   Commit style: Using VIM, begin each commit with the branch name, time and then descritpion of task completed. `PS-1 #time 30m Changed Header Logo to Bold` 
*   Example of this process will go as such:
    1. `git add .`
    2. `git commit`
        - inside VIM: `PS-1 #time 30m Changed Header Logo to Bold` 
    3. `git push origin PS-1`
*   Repeat this process until ticket is solved

## Developer Submits Ticket
*   Create pull request 
*   Review code with team during SCRUM meeting
*   If Accepted, ticket is merged into the branch
    * Branch deleted from remote. 
    * Jira status now set to `Staged`
*   If Rejected, continue working on ticket until the issues addressed are resolved. Then repeat above steps.

## Bundle New Changes up to Production
*   Jira status will now reflect `Visual QA` 

## IF Ticket Accepted
*   Delete the branch and move on to the next ticket

## IF Ticket Kicked Back
*   Delete the branch locally and remote. `git branch -D PS-1`
*   Clarify requirements
*   Pull the latest working master branch (i.e `initial_launch`)
*   Once branch is up to date, create new working branch with same ticket name/id
*   `git checkout -b PS-1`
*   Repeat steps above.
