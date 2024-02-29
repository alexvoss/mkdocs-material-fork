# Access management

----

- Guidelines on getting access
- Guidelines on managing access
  - Forking
  - Mirroring
  - Cloning
- Outside collaborators

----

    - How do I get access?
    - Access for Organizations
    - Sharing Access:
        - Forking
        - Mirroring
        - Cloning
    - Outside collaborators


[__How do I gain access to the private Insiders repository?__](#access-account){ #access-account }

If you sponsored with your __individual account__, you should have received an
email invitation to the private Material for MkDocs Insiders repository right
after you initiated your sponsorship. Simply accept the invitation within seven
days to gain access.

If you sponsored using an __organization account__, please note we need
an individual account that we can list as a collaborator of the private Insiders
repository. After you initiate your sponsorship, please email us at
sponsors@squidfunk.com with the name of the individual or bot account. Once you
provide us with this information, we will add the account as a collaborator, and
after you accept the invitation, you will gain access to the repository.

If you have yet to receive the email or the invitation link has expired, please
contact us, the maintainers, at sponsors@squidfunk.com. We're working on a
solution that will allow you to manage collaborator status yourself.

[__Why can't our whole organization get access to Insiders?__](#access-organization){ #access-organization }

Currently, it is not possible to grant access to an organizational account, as
GitHub only allows for adding individual user accounts. We are working on a
solution ourselves to simplify access for organizations. For now, to ensure that
access is not tied to a particular individual, we recommend creating a bot
account, i.e., a GitHub account that does not belong to a specific individual
but is listed as the owner of the organizational account and using this account
for sponsorship.

[__Do I need to fork the repository to use it?__](#access-fork){ #access-fork }

It depends. If you are using the Insiders edition as an individual, you can work
directly with the private repository, as you do not need to share the Insiders
features with others. If you are working with a team, it is best to create a
private [fork] using the individual account you listed as a collaborator of
Material for MkDocs to grant access to all members of your organization to
your fork.

[__Can I share my Insiders access with others?__](#access-share){ #access-share }

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


[__Can outside collaborators build and run the documentation locally without access to Insiders?__](#insiders-outside-collaborators){ #insiders-outside-collaborators }

Yes. Insiders is compatible with Material for MkDocs. Almost all new features
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
  [getting started guide]: ../getting-started.md#caveats
  [Card grids]: ../../reference/grids.md?h=grids#using-card-grids



[__We are hosting our repository on Gitlab, can we also use Insiders?__](#github-alternatives){ #github-alternatives }

Absolutely! Material for MkDocs Insiders is designed to be compatible with
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


[__Can outside collaborators build and run the documentation locally without access to Insiders?__](#insiders-outside-collaborators){ #insiders-outside-collaborators }

Yes. Insiders is compatible with Material for MkDocs. Almost all new features
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
  [getting started guide]: ../getting-started.md#caveats
  [Card grids]: ../../reference/grids.md?h=grids#using-card-grids
