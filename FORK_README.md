# geotoaddb

fork of https://github.com/steve8x8/geotoad

## Local Install

install both versions, geotoad and geotoaddb, locally.

    git clone https://github.com/SBejga/geotoaddb ~/Development/ruby/geotoad
    git clone https://github.com/SBejga/geotoaddb ~/Development/ruby/geotoaddb
    cd https://github.com/SBejga/geotoaddb ~/Development/ruby/geotoaddb
    git checkout mongo

Add Alias to your bash_profile

    alias geotoad='~/Development/ruby/geotoad/geotoad.rb'
    alias geotoaddb='~/Development/ruby/geotoaddb/geotoad.rb'

## Updating

when updating from base repository (steve8x8/geotoad) then, 
do it in ~/Development/ruby/geotoad

    cd ~/Development/ruby/geotoad

    # git remote add base https://github.com/steve8x8/geotoad

    git checkout master
    git pull base master
	
Do the merge:

- in most cases only check lib/version.rb
- update line with version

Commit

    git add lib/version.rb && git commit

And push changes to to my fork repo at master branch

    git push origin master
    
Do the rest at mongo branch at ~/Development/ruby/geotoaddb

    cd ~/Development/ruby/geotoaddb
    
    git checkout master
    git pull
    git checkout mongo
    git merge master

Do the merge

    git push
   
