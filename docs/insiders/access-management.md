# Access management

The Material for MkDocs Insiders repository is a private repository hosted on
GitHub access is, therefore, managed through GitHub itself. If you're wondering
how access is managed and how sharing your access with your team works, you'll
find everything you need to know on this page.

## How to get access

As the private Material for MkDocs Insiders repository is hosted on GitHub, you
require a GitHub account to become a sponsor and to gain access. After
sponsoring us on one of our [sponsoring tiers] starting at $15/monthly, we
prioritize providing you with immediate access to the private Material for
MkDocs Insiders repository. The process of gaining access is partially automated.
Depending on the type of account you've used to become a sponsor, we might need
more information from you before we can grant access.

  [sponsoring tiers]: sponsoring-tiers.md

### Individuals

If you sponsor using a [personal account], you will receive an invitation link
via email to the private Material for MkDocs Insiders repository immediately
after initiating your sponsorship. This invitation, automatically issued by
GitHub is valid for seven days. Once [accepted within this time], you'll be
ready to [get started].

  [personal account]: https://docs.github.com/en/get-started/learning-about-github/types-of-github-accounts#personal-accounts
  [accepted within this time]: #expired-invitations
  [get started]: installation.md

### Organizations

Sponsoring through an [organization account], please note that GitHub will not
send an invitation via email to access the private Material for MkDocs Insiders
repository due to [GitHub limitations]. It is not possible to grant access to an
[organization account]. Therefore, if you've sponsored using an organization
account, contact us at sponsors@squidfunk.com with the names of up to three
[personal accounts] or one [bot account] that is publicly or privately listed
as owners of your GitHub organization. We will add these designated accounts as
collaborators, and once the invitation is accepted within seven days, you'll be
all set to [get started].

  [organization account]: https://docs.github.com/en/get-started/learning-about-github/types-of-github-accounts#organization-accounts
  [GitHub limitations]: #collaborators
  [bot account]: #bot-account

### Enterprises

If you would like to sponsor us using an [enterprise account], we recommend
using a [personal account] or a [bot account] to initiate the sponsorship and
access the private Material for MkDocs Insiders repository using this account.

  [enterprise account]: https://docs.github.com/en/get-started/learning-about-github/types-of-github-accounts#enterprise-accounts

## Restrictions

GitHub sets limitations beyond our control, which is why we require further
information regarding [collaborators] and [matching].

  [collaborators]: #collaborators
  [matching]: #matching

### Collaborators

GitHub policy limits access to [private repositories] to [personal accounts]
only, which is why it is currently not possible for us to add [organization
accounts] to the Material for MkDocs Insiders repository, which is a private
repository. Therefore, it is not feasible for us to add each member of an
organization as collaborators.

  [private repositories]: https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository
  [personal accounts]: https://docs.github.com/en/get-started/learning-about-github/types-of-github-accounts#personal-accounts
  [organization accounts]: https://docs.github.com/en/get-started/learning-about-github/types-of-github-accounts#organization-accounts

### Matching

Due to privacy reasons, GitHub does not allow email addresses to be matched with
GitHub accounts. When requesting access via email at sponsors@squidfunk.com,
it's necessary to provide us with the name of a [personal account].

## Bot account

Given that only personal accounts can be listed as collaborators on
[private repositories], ensuring access for an entire organization requires
coordination through individuals. Changes within the team could lead to losing
access to the entire organization. To avoid this, you have two options:

  - Add multiple personal accounts as collaborators
  - Create and add a bot account, which is [a new personal account] that does
  not belong to a specific individual but is publicly or privately listed as the
  owner of the GitHub organization

Employing a bot account for access management and initiating your public or
[private] sponsorship offers a streamlined approach to handling all of your
sponsoring costs, allowing you to manage access and payment for all sponsorships
through a single account.

  [a new personal account]: https://docs.github.com/en/get-started/start-your-journey/creating-an-account-on-github
  [private]: privacy.md

## Expired invitations

If the invitation is not accepted within the period of seven days, you'll
need to contact us via mail at sponsors@squidfunk.com, and we will issue the
invitation to the private Material for MkDocs Insiders repository again.

## Team management

If you are using Material for MkDocs Insiders as an [Individual] and do not work
with a team, [forking] the private repository is not necessary. However, when
working with a team that would like to use the Material for MkDocs Insiders
features with you, it is – at this moment – not possible to share your
collaborator status with other accounts. In order to work in a team, the
personal or bot account holding collaborator access can [fork], [clone], or
[mirror] the private Material for MkDocs Insiders repository, providing a
pathway for team collaboration.

  [fork]: #forking
  [clone]: #cloning
  [mirror]: #mirroring
  [Individual]: #individuals

### Outside collaborators

When working with outside collaborators, you should know that the Insiders
edition is compatible with the Community edition. Almost all new features and
configuration options are either backward-compatible or implemented behind
feature flags. Changing the general appearance of your site should be optional.
Most Insiders features enhance the overall experience, e.g., by adding icons to
pages or providing a feedback widget. While these features add value for your
site's users, they should be optional for previewing when making changes to
content. Currently, the only content-related feature in Insiders that
non-Insiders users can't correctly preview is [Card grids].

This means that outside collaborators can build the documentation locally with
Material for MkDocs, and when they push their changes, your CI pipeline will
build it with Insiders. When using built-in plugins exclusive to Insiders, it's
recommended to split configuration into a base `mkdocs.yml` and one with plugin
overrides via [configuration inheritance]. See the [getting started guide] for
more information.

  [configuration inheritance]: https://www.mkdocs.org/user-guide/configuration/#configuration-inheritance
  [getting started guide]: installation.md
  [Card grids]: ../reference/grids.md?h=grids#using-card-grids


### Forking

[Forking] a repository creates a copy of the repository that allows for
independent development while maintaining a link to the original repository
for updates.

  [forking]: https://docs.github.com/en/get-started/quickstart/fork-a-repo

### Cloning

[Cloning] a repository copies the repository to your local machine or codespace,
facilitating offline work and content management. [Cloning your private fork] is
also an option for individualized control

  [cloning]: https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository
  [cloning your private fork]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo#cloning-your-forked-repository

### Mirroring

[Mirroring] a repository creates an identical copy, ensuring you have the
flexibility to host and work with the repository [in other environments] besides
GitHub.

  [mirroring]: https://docs.github.com/en/repositories/creating-and-managing-repositories/duplicating-a-repository
  [in other environments]: #github-alternatives

## GitHub alternatives

Material for MkDocs Insiders is designed to be compatible with various
repository hosting platforms, including GitLab. The key requirement is still a
GitHub account, as we use GitHub Sponsors for all transactions and manage access
to the private Insiders repository through GitHub.

Once you've become a sponsor and secured access to the private Insiders
repository via an individual GitHub account, you can [mirror the repository in
another location]. This mirroring process not only allows for easy integration
into your existing workflow but also ensures that your projects stay up-to-date
with the latest features and improvements of Material for MkDocs Insiders.

Our discussion board is a valuable resource for any questions about integrating
Material for MkDocs Insiders into your projects. It offers a space to connect
with others who may have similar requirements and setups, as well as to
exchange tips and explore solutions together.

  [mirror the repository in another location]: https://docs.github.com/en/repositories/creating-and-managing-repositories/duplicating-a-repository#mirroring-a-repository-in-another-location
  [discussion board]: https://github.com/squidfunk/mkdocs-material/discussions
