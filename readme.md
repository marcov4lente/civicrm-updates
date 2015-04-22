The updated sections of the code have been temporarily encapsed with

```
/* START CRM-xxxxxx UPDATES */
```

and

```
/* END CRM-xxxxxx UPDATES */
```

comments, in order to make it easier to see the changes

#CRM-15829

Add pending memberships to new members of an organisation that has pneding memberships

- CRM/Contact/BAO/Relationship - line 1459
- CRM/Contact/BAO/Relationship - line 1486
- CRM/Contact/BAO/Relationship - line 1494

Ensure these new pending memebrships for an organisations employees are not set to active

- CRM/Member/BAO/Membership - line 261

# CRM-15881

Clear current empployee when deleting a relationship that is the employer

- CRM/Contact/BAO/Relationship - line 623

Reload the tab ajax views to reflect removed employer display when deleting a relationship that is the employer

- CRM/Contact/BAO/Relationship - line 395

If disabling an employer relationship, unset the is_current_employer, please see comments in code

- CRM/Contact/BAO/Relationship - line 435

Updated query to use bound variables in the SQL query string, to prevent SQL injection

- CRM/Contact/BAO/Contact/Utils.php - line 457

