
### git commit --amend
: Changing the most recent commit BUT need to force push

-  usecases
	- add changes to last commit without editing its message

		`$ git add .`
		`$ git commit --amend --no-edit`

	- edit commit message
		`$ git commit --amend`
		or
		`$ git commit --amend -m "new commit message"`

### 