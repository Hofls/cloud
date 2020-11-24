* `My Billing Dashboard`
    * `Billing Preferences` check boxes:
        * `Receive PDF Invoice By Email`
        * `Receive Free Tier Usage Alerts`
            * Set `Email Address`
        * `Receive Billing Alerts`
    * `Budgets`:
        * `Create budget` -> `Cost budget`
            * Set `Budgeted amount` (e.g. $2) 
            * Set `threshold` (e.g. 80)
            * Set `Email recipients`
* `Cloudwatch`
    * `Alarms` -> `Billing` - `Create alarm`
    * `All` -> `Billing` -> `Total Estimated Charge`
    * Set `threshold` (e.g. $4)
    * `Create new SNS topic` -> Set email
* `IAM`
    * `Enable MFA`
    * `Add user` with fewer privileges than Administrator
    * 
