# Postprocessing

#### [functional][u] lift access restrictions to iso in openQA

iso downloads in openQA were disabled for he final build. the restrictions can be removed again after GM

#### openQA cleanup

- tag the GM build
- reduce job group size
- delete obsolete assets

#### tag/branch all translations in git

add tags or branches for all translations in git, in case they need to be updated from that specific branch later

* package-translations (git@github.com:openSUSE/packages-i18n.git)
* desktop-translations (git@github.com:openSUSE/desktop-file-translations.git)
* yast2-trans (git@github.com:yast/yast-translations.git)
* yast2-slide-show (git@github.com:openSUSE/yast-slide-show.git)
* skelcd-openSUSE (git@github.com:openSUSE/skelcd-openSUSE.git)
* openSUSE-EULAs (git@github.com:openSUSE/openSUSE-EULAs.git)

Example:
    $ osc ls openSUSE:Leap:15.1 skelcd-openSUSE | grep tar
    skelcd-openSUSE-84.87.20170712.1dc7ffa.tar.xz
    $ git show 1dc7ffa
    $ git tag Leap_15.1-GM 1dc7ffa
    $ git push origin Leap_15.1-GM
    Total 0 (delta 0), reused 0 (delta 0)
    To github.com:openSUSE/skelcd-openSUSE.git
    * [new tag]         Leap_15.1-GM -> Leap_15.1-GM



