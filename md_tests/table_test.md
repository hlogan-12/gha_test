| Branch Name | Branch Protection Rules | Notes/Justification |
| --- | --- | --- |
| pw_staging | <ul><li>- [x] Require a pull request before merging</li><ul><li>- [x] Require approvals (1)</li><li>- [x] Dismiss stale pull request approvals when new commits are pushed</li></ul><li>- [x] Require successful deployments to 'sgdev_pw' and 'sgqa_pw' environments</li></ul><br>_NOTE: "Do not allow bypassing the above settings" should NOT be checked._ |  |
| main |  |  |

<br><br>

<table style="width:100%">
  <tr>
    <th style="width:10%">Branch</th>
    <th style="width:40%">Protection Rules</th>
    <th style="width:60%">Notes</th>
  </tr>
  <tr>
    <td>staging</td>
    <td>&#9679;&nbsp; Require a pull request before merging<br>&nbsp;&nbsp;&nbsp;&#9702;&nbsp; Require approvals (1)<br>&nbsp;&nbsp;&nbsp;&#9702;&nbsp; Dismiss stale approvals when new commits pushed<br>&#9679;&nbsp; Require successful deployments to 'sgdev_pw' and 'sgqa_pw' environments </td>
    <td>Requiring successful deployments to dev/qa is required in most cases.  However, there are cases (e.g., documentation updates or updating non-functional code within target files) where we do not want to deploy our environments when the pull request is created, which will require approvers/admins to 'bypass' the 'Require successful deployments...' branch protection rule.  Pull requests to the staging branach should have a review/approval in all cases.</td>
  </tr>
  <tr>
    <td>main</td>
    <td>&#9679;&nbsp; Require a pull request before merging<br>&nbsp;&nbsp;&nbsp;&#9702;&nbsp; Require approvals (1)<br>&nbsp;&nbsp;&nbsp;&#9702;&nbsp; Dismiss stale pull request approvals when new commits are pushed<br>&#9679;&nbsp; Do not allow bypassing the above settings</td>
    <td>The prd pw rotation deployment is not initiated until the pull request has been merged to main, so the environment deployment rule is not required.</td>
  </tr>
</table>
