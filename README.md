# library-of-babel
Emacs org mode library of babel

## In this repo i'm attempting to create a cleaned-up, centralized version of my org-babel script block library.

To add this to your emacs, run

~~~
cd ~./.emacs.d/
git clone https://github.com/AlexStragies/library-of-babel
~~~

Then, add this block to your emacs startup file:

~~~
(funcall (lambda (dir)
           (if (file-directory-p dir)
               (mapcar (lambda (file) (org-babel-lob-ingest file))
                       (directory-files dir t ".+\\.org?$" t ))))
         "~/.emacs.d/library-of-babel")
~~~

The above block finds all org-mode files under ~/.emacs.d/library-of-babel/, and ingests them into the library.

## File organisation

Multiple files make it easier to ...