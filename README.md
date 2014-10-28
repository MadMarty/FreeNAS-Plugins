#PREPARATION

* The ports in ./ports should be copied into your ports tree
    - <code>cp -R ports/* /usr/ports/</code>

* Some user(s) and group(s) need to be added to '/usr/ports/UIDs' and '/usr/ports/GIDs' before compiling Ports or PBIs.

    - /usr/ports/UIDs
        - <code>syncthing:*:815:815::0:0:Syncthing Daemon:/nonexistent:/usr/sbin/nologin</code>
        - <code>media:*:816:816::0:0:Media Plugins Daemon:/nonexistent:/usr/sbin/nologin</code>

    - /usr/ports/GIDs
        - <code>syncthing:*:815:</code>
        - <code>media:*:816:</code>

* Compile
    - <code>pbi_makeport -c ./plugins/madsonic -o ./pbi --pkgdir ./pkg/madsonic</code>
    - <code>pbi_makeport -c ./plugins/subsonic -o ./pbi --pkgdir ./pkg/subsonic</code>
    - <code>pbi_makeport -c ./plugins/syncthing -o ./pbi --pkgdir ./pkg/syncthing</code>
