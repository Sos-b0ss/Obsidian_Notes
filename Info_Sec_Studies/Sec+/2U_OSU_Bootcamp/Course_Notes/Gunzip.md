
using [[Gunzip]] & [[gzip]] it will make a [[zip.gz]] file as the result.

include [[BUP]] from .snar

use this command:

[[tar]] cvvWf {<emerg_back_sun.tar>} --listed-incremental={ermg_backup.snar} --level=0 emergency

[[tar]] tvvf {emerg_BUP.tar} --incremental

--level=0 is the way to start a [[full BUP]] so as to be usable for [[incremental BUPS]]

standard for [[BUPS]] name format
year/month/date<name>

-c{dir_of_BUP} <- this will put you in the dir so you dont need the absolute path
