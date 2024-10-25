# pihole-whitelist

This was a quick project to make a list of commonly whitelisted domains derived from this pihole fourm post: <https://discourse.pi-hole.net/t/commonly-whitelisted-domains/212)https://discourse.pi-hole.net/t/commonly-whitelisted-domains/212>

The raw whitelist is here <https://raw.githubusercontent.com/cedwards4038/pihole-whitelist/main/whitelist.txt>

My Version for AdGuard is Here: <https://github.com/cedwards4038/adguard-whitelist/tree/main>

You should be able to copy this codeblock to add everything pihole whitelist at once

```SHELL
#Reddit
pihole --white-regex [a-z]\.thumbs\.redditmedia\.com
pihole --white-regex (\.|^)redd\.it$
pihole --white-regex (\.|^)reddit\.com$

#WhatsApp
pihole --white-regex ^whatsapp-cdn-shv-[0-9]{2}-[a-z]{3}[0-9]\.fbcdn\.net$
pihole --white-regex ^((www|(w[0-9]\.)?web|media((-[a-z]{3}|\.[a-z]{4})[0-9]{1,2}-[0-9](\.|-)(cdn|fna))?)\.)?whatsapp\.(com|net)$

#Skype
pihole -w s1.symcb.com s2.symcb.com s3.symcb.com s4.symcb.com s5.symcb.com

#Google (Maps, Youtube, etc)

#Google Maps and other Google Services
pihole -w clients4.google.com
pihole -w clients2.google.com

#Youtube History
pihole -w s.youtube.com
pihole -w video-stats.l.google.com

#Youtube App for iOS/iPadOS
pihole -w www.googleapis.com
pihole -w youtubei.googleapis.com
pihole -w oauthaccountmanager.googleapis.com

#Google Play
pihole -w android.clients.google.com

#Google Keep
pihole -w reminders-pa.googleapis.com
pihole -w firestore.googleapis.com

#Google Fonts
pihole -w gstaticadssl.l.google.com

#Gmail
pihole -w googleapis.l.google.com

#Google Chrome(to update on ubuntu)
pihole -w dl.google.com

#Android TV
pihole -w redirector.gvt1.com

#Microsoft (Windows, Office, Skype, etc)

#Windows uses this to verify connectivity to Internet
pihole -w www.msftncsi.com
pihole -w www.msftconnecttest.com

#Microsoft Web Pages (Outlook, Office365, Live, Microsoft.com...)
pihole -w outlook.office365.com
pihole -w products.office.com
pihole -w c.s-microsoft.com
pihole -w i.s-microsoft.com
pihole -w login.live.com
pihole -w login.microsoftonline.com

#Backup bitlocker recovery key to Microsoft account
pihole -w g.live.com

#Microsoft Store (Windows Store)
pihole -w dl.delivery.mp.microsoft.com
pihole -w geo-prod.do.dsp.mp.microsoft.com
pihole -w displaycatalog.mp.microsoft.com

#Windows 10 Update
pihole -w sls.update.microsoft.com.akadns.net
pihole -w fe3.delivery.dsp.mp.microsoft.com.nsatc.net
pihole -w tlu.dl.delivery.mp.microsoft.com

#Microsoft Edge Browser Update
pihole -w msedge.api.cdp.microsoft.com

#Skype
pihole -w s.gateway.messenger.live.com
pihole -w client-s.gateway.messenger.live.com
pihole -w ui.skype.com
pihole -w pricelist.skype.com
pihole -w apps.skype.com
pihole -w m.hotmail.com
pihole -w sa.symcb.com
pihole -w s1.symcb.com s2.symcb.com s3.symcb.com s4.symcb.com s5.symcb.com

#Microsoft Office
pihole -w officeclient.microsoft.com

#Bing Maps Platform
pihole -w dev.virtualearth.net
pihole -w ecn.dev.virtualearth.net
pihole -w t0.ssl.ak.dynamic.tiles.virtualearth.net
pihole -w t0.ssl.ak.tiles.virtualearth.net

#Xbox

#Xbox Live
pihole -w clientconfig.passport.net
#Xbox Live Achievements (confirmed by Microsoft)
pihole -w v10.events.data.microsoft.com
pihole -w v20.events.data.microsoft.com

#Xbox Live Messaging
pihole -w client-s.gateway.messenger.live.com

#Store App on Series X/S
pihole -w arc.msn.com

#EA Play on Xbox
pihole -w activity.windows.com

#Full Functionality
pihole -w xbox.ipv6.microsoft.com
pihole -w device.auth.xboxlive.com
pihole -w www.msftncsi.com
pihole -w title.mgt.xboxlive.com
pihole -w xsts.auth.xboxlive.com
pihole -w title.auth.xboxlive.com
pihole -w ctldl.windowsupdate.com
pihole -w attestation.xboxlive.com
pihole -w xboxexperiencesprod.experimentation.xboxlive.com
pihole -w xflight.xboxlive.com
pihole -w cert.mgt.xboxlive.com
pihole -w xkms.xboxlive.com
pihole -w def-vef.xboxlive.com
pihole -w notify.xboxlive.com
pihole -w help.ui.xboxlive.com
pihole -w licensing.xboxlive.com
pihole -w eds.xboxlive.com
pihole -w www.xboxlive.com
pihole -w v10.vortex-win.data.microsoft.com
pihole -w settings-win.data.microsoft.com
pihole -w catalog.gamepass.com
pihole -w go.microsoft.com
pihole -w dmd.metaservices.microsoft.com

#Apple

#Apple Music
pihole -w itunes.apple.com
pihole -w s.mzstatic.com

#Apple ID
pihole -w appleid.apple.com

#iOS Weather App
pihole -w gsp-ssl.ls.apple.com
pihole -w gsp-ssl.ls-apple.com.akadns.net

#Captive Portal Tests

#Android/Chrome
pihole -w connectivitycheck.android.com
pihole -w android.clients.google.com
pihole -w clients3.google.com
pihole -w connectivitycheck.gstatic.com

#Windows/Microsoft
pihole -w msftncsi.com
pihole -w www.msftncsi.com
pihole -w ipv6.msftncsi.com

#iOS/Apple
pihole -w captive.apple.com
pihole -w gsp1.apple.com
pihole -w www.apple.com
pihole -w www.appleiphonecell.com

#Other Domains

#Spotify
#for iOS
pihole -w spclient.wg.spotify.com
pihole -w apresolve.spotify.com
#for tv apps
pihole -w api-tv.spotify.com

#Target Weekly Ads
pihole -w weeklyad.target.com
pihole -w m.weeklyad.target.com
pihole -w weeklyad.target.com.edgesuite.net

#Facebook/Facebook Messenger
pihole -w upload.facebook.com
pihole -w creative.ak.fbcdn.net
pihole -w external-lhr0-1.xx.fbcdn.net
pihole -w external-lhr1-1.xx.fbcdn.net
pihole -w external-lhr10-1.xx.fbcdn.net
pihole -w external-lhr2-1.xx.fbcdn.net
pihole -w external-lhr3-1.xx.fbcdn.net
pihole -w external-lhr4-1.xx.fbcdn.net
pihole -w external-lhr5-1.xx.fbcdn.net
pihole -w external-lhr6-1.xx.fbcdn.net
pihole -w external-lhr7-1.xx.fbcdn.net
pihole -w external-lhr8-1.xx.fbcdn.net
pihole -w external-lhr9-1.xx.fbcdn.net
pihole -w fbcdn-creative-a.akamaihd.net
pihole -w scontent-lhr3-1.xx.fbcdn.net
pihole -w scontent.xx.fbcdn.net
pihole -w scontent.fgdl5-1.fna.fbcdn.net
pihole -w graph.facebook.com
pihole -w b-graph.facebook.com
pihole -w connect.facebook.com
pihole -w cdn.fbsbx.com
pihole -w api.facebook.com
pihole -w edge-mqtt.facebook.com
pihole -w mqtt.c10r.facebook.com
pihole -w portal.fb.com
pihole -w star.c10r.facebook.com
pihole -w star-mini.c10r.facebook.com
pihole -w b-api.facebook.com
pihole -w fb.me
pihole -w bigzipfiles.facebook.com
pihole -w l.facebook.com
pihole -w www.facebook.com
pihole -w scontent-atl3-1.xx.fbcdn.net
pihole -w static.xx.fbcdn.net
pihole -w edge-chat.messenger.com
pihole -w video.xx.fbcdn.net
pihole -w external-ort2-1.xx.fbcdn.net
pihole -w scontent-ort2-1.xx.fbcdn.net
pihole -w edge-chat.facebook.com
pihole -w scontent-mia3-1.xx.fbcdn.net
pihole -w web.facebook.com
pihole -w rupload.facebook.com
pihole -w l.messenger.com

#DirectTV
pihole -w directvnow.com
pihole -w directvapplications.hb.omtrdc.net
pihole -w s.zkcdn.net
pihole -w js.maxmind.com

#Bild DE
pihole -w www.asadcdn.com
pihole -w code.bildstatic.de
pihole -w de.ioam.de
pihole -w json.bild.de
pihole -w script.ioam.de
pihole -w tags.tiqcdn.com
pihole -w tagger.opecloud.com

#Plex Domains
pihole -w plex.tv
pihole -w tvdb2.plex.tv
pihole -w pubsub.plex.bz
pihole -w proxy.plex.bz
pihole -w proxy02.pop.ord.plex.bz
pihole -w cpms.spop10.ams.plex.bz
pihole -w meta-db-worker02.pop.ric.plex.bz
pihole -w meta.plex.bz
pihole -w tvthemes.plexapp.com.cdn.cloudflare.net
pihole -w tvthemes.plexapp.com
pihole -w 106c06cd218b007d-b1e8a1331f68446599e96a4b46a050f5.ams.plex.services
pihole -w meta.plex.tv
pihole -w cpms35.spop10.ams.plex.bz
pihole -w proxy.plex.tv
pihole -w metrics.plex.tv
pihole -w pubsub.plex.tv
pihole -w status.plex.tv
pihole -w www.plex.tv
pihole -w node.plexapp.com
pihole -w nine.plugins.plexapp.com
pihole -w staging.plex.tv
pihole -w app.plex.tv
pihole -w o1.email.plex.tv
pihole -w o2.sg0.plex.tv
pihole -w dashboard.plex.tv
#Custom Login Pictures
pihole -w gravatar.com
#TV Series Metadata
pihole -w thetvdb.com
#Movie Metadata
pihole -w themoviedb.com
#iHeart radio/Plex Podcast
pihole -w chtbl.com

#Sonarr
pihole -w services.sonarr.tv
pihole -w skyhook.sonarr.tv
pihole -w download.sonarr.tv
pihole -w apt.sonarr.tv
pihole -w forums.sonarr.tv

#Placehold.it (Image placeholders often used during web design.)
pihole -w placehold.it
pihole -w placeholdit.imgix.net

#Dropbox
pihole -w dl.dropboxusercontent.com
pihole -w ns1.dropbox.com
pihole -w ns2.dropbox.com

#Fox News
pihole -w widget-cdn.rpxnow.com

#Images on Marketwatch.com
pihole -w s.marketwatch.com

#GoDaddy webmail buttons
pihole -w imagesak.secureserver.net

#WatchESPN
pihole -w fpdownload.adobe.com
pihole -w entitlement.auth.adobe.com
pihole -w livepassdl.conviva.com

#NVIDIA GeForce Experience
pihole -w gfwsl.geforce.com

#Videos not playing in times.com and nydailynews.com
pihole -w delivery.vidible.tv
pihole -w img.vidible.tv
pihole -w videos.vidible.tv
pihole -w edge.api.brightcove.com
pihole -w cdn.vidible.tv

#Videos not playing on weather.com
pihole -w v.w-x.co

#Moto phones OS updates
pihole -w appspot-preview.l.google.com

#Grand Theft Auto V Online PC
pihole -w prod.telemetry.ros.rockstargames.com

#Chevrolet
pihole -w chevrolet.com

#Epic Games Store
pihole -w tracking.epicgames.com

#Origin (Savegame-Sync)
pihole -w cloudsync-prod.s3.amazonaws.com

#Red Hat Online Learning (subscription required)
pihole -w 79423.analytics.edgekey.net

#Lowe's Checkout
pihole -w assets.adobedtm.com

#Home Depot Checkout
pihole -w nexus.ensighten.com

#Mozilla Firefox Tracking Protection
pihole -w tracking-protection.cdn.mozilla.net

#Playstation 5 "Recently Played Games" and Trophies
pihole -w telemetry-console.api.playstation.com

#Cannon Printers
pihole -w gdlp01.c-wss.com

#Reddit
pihole -w styles.redditmedia.com
pihole -w www.redditstatic.com
pihole -w reddit.map.fastly.net
pihole -w www.redditmedia.com
pihole -w reddit-uploaded-media.s3-accelerate.amazonaws.com
pihole -w thumbs.redditmedia.com
pihole -w redd.it
pihole -w reddit.com

#Reddit Regex Whitelist
pihole --white-regex [a-z]\.thumbs\.redditmedia\.com
pihole --white-regex (\.|^)redd\.it$
pihole --white-regex (\.|^)reddit\.com$

#Tracking Packages sent with DPD
pihole -w tracking.dpd.de

#WhatsApp
pihole -w wa.me

#WhatsApp Regex Whitelist
pihole --white-regex ^whatsapp-cdn-shv-[0-9]{2}-[a-z]{3}[0-9]\.fbcdn\.net$
pihole --white-regex ^((www|(w[0-9]\.)?web|media((-[a-z]{3}|\.[a-z]{4})[0-9]{1,2}-[0-9](\.|-)(cdn|fna))?)\.)?whatsapp\.(com|net)$

#Signal
pihole -w ud-chat.signal.org
pihole -w chat.signal.org
pihole -w storage.signal.org
pihole -w signal.org
pihole -w www.signal.org
pihole -w updates2.signal.org
pihole -w textsecure-service-whispersystems.org
pihole -w giphy-proxy-production.whispersystems.org
pihole -w cdn.signal.org
pihole -w whispersystems-textsecure-attachments.s3-accelerate.amazonaws.com
pihole -w d83eunklitikj.cloudfront.net
pihole -w souqcdn.com
pihole -w cms.souqcdn.com
pihole -w api.directory.signal.org
pihole -w contentproxy.signal.org
pihole -w turn1.whispersystems.org

#X/Twitter
pihole -w twitter.com
pihole -w upload.twitter.com
pihole -w api.twitter.com
pihole -w mobile.twitter.com
pihole -w twimg.com

#TikTok
pihole -w tiktokcdn.com
pihole -w tiktokcdn-us.com
pihole -w mssdk-va.tiktok.com

#Banks

#TBS Mobile
pihole -w h-sdk.online-metrix.net
pihole -w check2.tsb.co.uk

#Citizen's Bank
pihole -w p11.techlab-cdn.com

#OLA Money
pihole -w logs.juspay.in

#Resturants / Rewards

#Burger King
pihole -w appboy-images.com
pihole -w rest.iad-03.braze.com

#Punchh (Farmer Boys, El Pollo Loco, Capriotti's, etc.)
pihole -w mobileandroidapi.punchh.com

#Rumble
pihole -w rmbl.ws

#Dutch / The Netherlands websites

#nu.nl (enable videos, tvgids et cetera)
pihole -w cds.s5x3j6q5.hwcdn.net

#Swedish streaming services

#svtplay (enable continuing where you left off)
pihole -w analytics.svt.se

#Paramount+

pihole -w cbsinteractive.hb.omtrdc.net
pihole -w scribe.logs.roku.com
#really don't like allowing this one, but it's what makes paramount+ work per https://www.reddit.com/r/pihole/comments/lxnjdg/comment/imj4g8m/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button
pihole -w pubads.g.doubleclick.net
pihole -w pagead2.googlesyndication.com

#iDrive (A Dropbox Alternative)
pihole -w ping-app1.idrive.com
pihole -w app.idrive.com
pihole -w idrive.com

```
