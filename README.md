allocine
============

A module to use Allocine API V3 in Python.

More details on the API usage at http://wiki.gromez.fr/dev/api/allocine_v3

A PHP version is available at https://github.com/gromez/allocine-api

Usage:

        from allocine import allocine
        api = allocine()
        api.configure('100043982026','29d185d98c984a359e6e6f26a0474269')
        
        movie = api.get(27405)
        print "Movie Title [{0}]".format(movie['movie']['originalTitle'])
        
        serie = api.tvseries(223)
        print "Serie Title [{0}]".format(serie['tvseries']['originalTitle'])
        
        season = api.season(12277)
        print "Season Number [{0}]".format(season['season']['seasonNumber'])
        
        episode = api.episode(247699)
        print "Episode Number [{0}]".format(episode['episode']['episodeNumberSeason'])
