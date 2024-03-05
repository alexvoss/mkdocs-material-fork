# Access management


## How to get access

### Individuals

If you sponsor using a [personal GitHub account], you will receive an invitation
link via mail to the private [Material for MkDocs Insiders repository]
immediatley after initiating your sponsorship. This invitation will
automatically be issued by GitHub. The invitation is valid for seven days and
once you accept it you'll be all set to [get started].

  [personal GitHub account]: https://docs.github.com/en/get-started/learning-about-github/types-of-github-accounts#personal-accounts
  [Material for MkDocs Insiders repository]: https://github.com/squidfunk/mkdocs-material-insiders
  [get started]: ../toolkit/insiders-installation.md

### Organizations

If you sponsor using an [organization GitHub account], please note that GitHub
will not issue an invitation to the private
[Material for MkDocs Insiders repository] via mail. It is at this moment
__not possible__ to grant access to an organizational account, due to
[GitHub limitations].

Therefore, after you initiate your sponsorship, please provide us with the name
of a [personal GitHub account] or a [bot account] which is publicly or privately
listed as an owner of your GitHub organization via mail at sponsors@squidfunk.com.
Once you provide us with the account name, we will add the account as a
collaborator and you'll be all set to [get started].

  [organization GitHub account]: https://docs.github.com/en/get-started/learning-about-github/types-of-github-accounts#organization-accounts
  [GitHub limitations]: #collaborators
  [bot account]: #bot-account

### Enterprises

If you would like to sponsor using an GitHub Enterprise account, we'd recommend
using a [personal GitHub account] or set up a [bot account]


Currently not possible to sponsor as an enterprise nor is it possible to add
GitHub organizations or GitHub Enterprises to private GitHub repositories.

## GitHub limitations

### Collaborators



Currently, it is not possible to grant access to an organizational account, as
GitHub only allows for adding individual user accounts. To ensure that access is
not tied to a particular individual, we recommend creating a bot accsount, i.e.,
a GitHub account that does not belong to a specific individual but is listed as
the owner of the organizational account and using this account for sponsorship.



It's currently not possible to grant access to each member of an organization,
as GitHub only allows for adding users. Thus, after sponsoring, please send an
email to sponsors@squidfunk.com, stating which account should become a
collaborator of the Insiders repository. To ensure that access is not tied to a
particular individual GitHub account, create a bot account (i.e. a GitHub
account that is not tied to a specific individual), and use this account for the
sponsoring. After being added to the list of collaborators, the bot account can
create a private fork of the private Insiders GitHub repository, and grant
access to all members of the organizations.


https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository

### Matching

No matching of email addresses and GitHub accounts

### Waitlist

No sponsoring for


## Bot account

## Expired invitations

If the invitation is not accepted within the time period of seven days, you'll
need to contact us via mail at sponsors@squidfunk.com and we will issue the
invitation once again.

## Team management

At the moment, it is not possible to directly share your collaborator status
for the private Insiders repository with other accounts. However, if you are
working with a team and would like them to access Insiders, you can share the
Insiders repository by utilizing options such as [cloning], [forking], or
[mirroring]. By doing so, you can start collaborating with your team members on
the new repository you have shared. This way, you can collectively benefit
from the Insiders features and work together on the project.

  [cloning]: https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository
  [forking]: https://docs.github.com/en/get-started/quickstart/fork-a-repo
  [mirroring]: https://docs.github.com/en/repositories/creating-and-managing-repositories/duplicating-a-repository

- Do I need to fork the repository to use it?

It depends. If you are using the Insiders edition as an individual, you can work
directly with the private repository, as you do not need to share the Insiders
features with others. If you are working with a team, it is best to create a
private [fork] using the individual account you listed as a collaborator of
Material for MkDocs to grant access to all members of your organization to
your fork.

### Forking

### Cloning

### Mirroring

### Outside collaborators

Insiders is compatible with Material for MkDocs. Almost all new features
and configuration options are either backward-compatible or implemented behind
feature flags. When working with outside collaborators, changing the general
appearance of your site should be optional. Most Insiders features enhance the
overall experience, e.g., by adding icons to pages or providing a feedback
widget. While these features add value for your site's users, they should be
optional for previewing when making changes to content. Currently, the only
content-related feature in Insiders that non-Insiders users can't properly
preview are [Card grids].

This means that outside collaborators can build the documentation locally with
Material for MkDocs, and when they push their changes, your CI pipeline will
build it with Insiders. When using built-in plugins exclusive to Insiders, it's
recommended to split configuration into a base `mkdocs.yml` and one with plugin
overrides via [configuration inheritance].

See the [getting started guide] for more information.

  [configuration inheritance]: https://www.mkdocs.org/user-guide/configuration/#configuration-inheritance
  [getting started guide]: ../toolkit/insiders-installation.md#caveats
  [Card grids]: ../../reference/grids.md?h=grids#using-card-grids


## GitHub alternatives

Material for MkDocs Insiders is designed to be compatible with
various repository hosting platforms, including GitLab. The key requirement is
still a GitHub account, as we use GitHub Sponsors for all transactions and
manage access to the private Insiders repository through GitHub.

Once you've become a sponsor and secured access to the private Insiders
repository via an individual GitHub account, you can
[mirror the repository in another location]. This mirroring process not only
allows for easy integration into your existing workflow but also ensures that
your projects stay up-to-date with the latest features and improvements of
Material for MkDocs Insiders.

For any questions about integrating Material for MkDocs Insiders into your
projects, our [discussion board] is a valuable resource. It offers a space to
connect with others who may have similar requirements and setups as well as to
exchange tips, and explore solutions together.

  [mirror the repository in another location]: https://docs.github.com/en/repositories/creating-and-managing-repositories/duplicating-a-repository#mirroring-a-repository-in-another-location
