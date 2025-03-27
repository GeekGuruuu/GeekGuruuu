 Activity: Add a test workflow

1. Open a new browser tab, and work through the following steps in that tab while you read the instructions in this tab.
1. Go to the **Actions tab**.
1. Click **New workflow**.
1. Search for "Simple workflow" and click **Configure**.
1. Name your workflow `ci.yml`.
1. Update the workflow by deleting the last two steps.
1. Add the following step at the end of your workflow:
   ```yml
   - name: Run markdown lint
     run: |
       npm install remark-cli remark-preset-lint-consistent
       npx remark . --use remark-preset-lint-consistent --frail
   ```
   > Even after the code is indented properly in `ci.yml`, you will see a build error in GitHub Actions. We'll fix this in the next step.
1. Click **Commit changes...**, and choose to make a new branch named `ci`.
1. Click **Propose changes**.
1. Click **Create pull request**.
1. Wait about 20 seconds and then refresh this page (the one you're following instructions from). [GitHub Actions](https://docs.github.com/actions) will automatically update to the next step.

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/test-with-actions) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2023 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>
