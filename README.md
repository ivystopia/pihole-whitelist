# pihole-whitelist

This was a quick project to make a list of commonly whitelisted domains derived from this pihole fourm post: <https://discourse.pi-hole.net/t/commonly-whitelisted-domains/212)https://discourse.pi-hole.net/t/commonly-whitelisted-domains/212>

The raw whitelist is here
<https://raw.githubusercontent.com/cedwards4038/pihole-whitelist/main/whitelist.txt>

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
pihole -w s{1..5}.symcb.com 


#Google (Maps, Youtube, etc)

#Google Maps and other Google Services
clients4.google.com
clients2.google.com

#Youtube History
s.youtube.com 
video-stats.l.google.com

#Youtube App for iOS/iPadOS
www.googleapis.com 
youtubei.googleapis.com
oauthaccountmanager.googleapis.com

#Google Play
android.clients.google.com

#Google Keep
reminders-pa.googleapis.com
firestore.googleapis.com

#Google Fonts
gstaticadssl.l.google.com

#Gmail
googleapis.l.google.com

#Google Chrome(to update on ubuntu)
dl.google.com

#Android TV
redirector.gvt1.com


#Microsoft (Windows, Office, Skype, etc)

#Windows uses this to verify connectivity to Internet
www.msftncsi.com 
www.msftconnecttest.com

#Microsoft Web Pages (Outlook, Office365, Live, Microsoft.com...)
outlook.office365.com 
products.office.com 
c.s-microsoft.com 
i.s-microsoft.com 
login.live.com 
login.microsoftonline.com 

#Backup bitlocker recovery key to Microsoft account
g.live.com

#Microsoft Store (Windows Store)
dl.delivery.mp.microsoft.com 
geo-prod.do.dsp.mp.microsoft.com 
displaycatalog.mp.microsoft.com

#Windows 10 Update
sls.update.microsoft.com.akadns.net 
fe3.delivery.dsp.mp.microsoft.com.nsatc.net 
tlu.dl.delivery.mp.microsoft.com

#Microsoft Edge Browser Update
msedge.api.cdp.microsoft.com

#Skype
s.gateway.messenger.live.com 
client-s.gateway.messenger.live.com 
ui.skype.com pricelist.skype.com 
apps.skype.com 
m.hotmail.com 
sa.symcb.com 
s{1..5}.symcb.com 

#Microsoft Office
officeclient.microsoft.com

#Bing Maps Platform
dev.virtualearth.net 
ecn.dev.virtualearth.net 
t0.ssl.ak.dynamic.tiles.virtualearth.net 
t0.ssl.ak.tiles.virtualearth.net

#Xbox

#Xbox Live
clientconfig.passport.net 
#Xbox Live Achievements (confirmed by Microsoft)
v10.events.data.microsoft.com
v20.events.data.microsoft.com

#Xbox Live Messaging
client-s.gateway.messenger.live.com

#Store App on Series X/S
arc.msn.com

#EA Play on Xbox
activity.windows.com

#Full Functionality
xbox.ipv6.microsoft.com 
device.auth.xboxlive.com 
www.msftncsi.com 
title.mgt.xboxlive.com 
xsts.auth.xboxlive.com 
title.auth.xboxlive.com 
ctldl.windowsupdate.com 
attestation.xboxlive.com 
xboxexperiencesprod.experimentation.xboxlive.com 
xflight.xboxlive.com 
cert.mgt.xboxlive.com 
xkms.xboxlive.com 
def-vef.xboxlive.com 
notify.xboxlive.com 
help.ui.xboxlive.com 
licensing.xboxlive.com 
eds.xboxlive.com 
www.xboxlive.com 
v10.vortex-win.data.microsoft.com 
settings-win.data.microsoft.com

#Apple

#Apple Music
itunes.apple.com
s.mzstatic.com

#Apple ID
appleid.apple.com

#iOS Weather App
gsp-ssl.ls.apple.com
gsp-ssl.ls-apple.com.akadns.net


#Captive Portal Tests

#Android/Chrome
connectivitycheck.android.com 
android.clients.google.com 
clients3.google.com 
connectivitycheck.gstatic.com 

#Windows/Microsoft
msftncsi.com 
www.msftncsi.com 
ipv6.msftncsi.com

#iOS/Apple
captive.apple.com 
gsp1.apple.com 
www.apple.com 
www.appleiphonecell.com


#Other Domains

#Spotify
#for iOS
spclient.wg.spotify.com 
apresolve.spotify.com
#for tv apps
api-tv.spotify.com

#Target Weekly Ads
weeklyad.target.com 
m.weeklyad.target.com 
weeklyad.target.com.edgesuite.net

#Facebook/Facebook Messenger
upload.facebook.com 
creative.ak.fbcdn.net 
external-lhr0-1.xx.fbcdn.net 
external-lhr1-1.xx.fbcdn.net 
external-lhr10-1.xx.fbcdn.net 
external-lhr2-1.xx.fbcdn.net 
external-lhr3-1.xx.fbcdn.net 
external-lhr4-1.xx.fbcdn.net 
external-lhr5-1.xx.fbcdn.net 
external-lhr6-1.xx.fbcdn.net 
external-lhr7-1.xx.fbcdn.net 
external-lhr8-1.xx.fbcdn.net 
external-lhr9-1.xx.fbcdn.net 
fbcdn-creative-a.akamaihd.net 
scontent-lhr3-1.xx.fbcdn.net 
scontent.xx.fbcdn.net 
scontent.fgdl5-1.fna.fbcdn.net 
graph.facebook.com 
b-graph.facebook.com 
connect.facebook.com 
cdn.fbsbx.com 
api.facebook.com 
edge-mqtt.facebook.com 
mqtt.c10r.facebook.com 
portal.fb.com 
star.c10r.facebook.com 
star-mini.c10r.facebook.com 
b-api.facebook.com 
fb.me 
bigzipfiles.facebook.com 
l.facebook.com 
www.facebook.com 
scontent-atl3-1.xx.fbcdn.net 
static.xx.fbcdn.net 
edge-chat.messenger.com 
video.xx.fbcdn.net 
external-ort2-1.xx.fbcdn.net 
scontent-ort2-1.xx.fbcdn.net 
edge-chat.facebook.com 
scontent-mia3-1.xx.fbcdn.net
web.facebook.com 
rupload.facebook.com 
l.messenger.com

#DirectTV
directvnow.com 
directvapplications.hb.omtrdc.net 
s.zkcdn.net 
js.maxmind.com

#Bild DE
www.asadcdn.com 
code.bildstatic.de 
de.ioam.de 
json.bild.de 
script.ioam.de 
tags.tiqcdn.com 
tagger.opecloud.com

#Plex Domains
plex.tv 
tvdb2.plex.tv 
pubsub.plex.bz 
proxy.plex.bz 
proxy02.pop.ord.plex.bz 
cpms.spop10.ams.plex.bz 
meta-db-worker02.pop.ric.plex.bz 
meta.plex.bz 
tvthemes.plexapp.com.cdn.cloudflare.net 
tvthemes.plexapp.com 
106c06cd218b007d-b1e8a1331f68446599e96a4b46a050f5.ams.plex.services 
meta.plex.tv 
cpms35.spop10.ams.plex.bz 
proxy.plex.tv 
metrics.plex.tv 
pubsub.plex.tv 
status.plex.tv
www.plex.tv 
node.plexapp.com 
nine.plugins.plexapp.com 
staging.plex.tv 
app.plex.tv 
o1.email.plex.tv  
o2.sg0.plex.tv 
dashboard.plex.tv
#Custom Login Pictures
gravatar.com
#TV Series Metadata
thetvdb.com
#Movie Metadata
themoviedb.com
#iHeart radio/Plex Podcast
chtbl.com

#Sonarr
services.sonarr.tv 
skyhook.sonarr.tv 
download.sonarr.tv 
apt.sonarr.tv 
forums.sonarr.tv

#Placehold.it (Image placeholders often used during web design.)
placehold.it 
placeholdit.imgix.net

#Dropbox
dl.dropboxusercontent.com 
ns1.dropbox.com 
ns2.dropbox.com

#Fox News
widget-cdn.rpxnow.com

#Images on Marketwatch.com
s.marketwatch.com

#GoDaddy webmail buttons
imagesak.secureserver.net

#WatchESPN
fpdownload.adobe.com 
entitlement.auth.adobe.com 
livepassdl.conviva.com

#NVIDIA GeForce Experience
gfwsl.geforce.com

#Videos not playing in times.com and nydailynews.com
delivery.vidible.tv 
img.vidible.tv 
videos.vidible.tv 
edge.api.brightcove.com 
cdn.vidible.tv

#Videos not playing on weather.com
v.w-x.co

#Moto phones OS updates
appspot-preview.l.google.com

#Grand Theft Auto V Online PC
prod.telemetry.ros.rockstargames.com

#Chevrolet
chevrolet.com

#Epic Games Store
tracking.epicgames.com

#Origin (Savegame-Sync)
cloudsync-prod.s3.amazonaws.com

#Red Hat Online Learning (subscription required)
79423.analytics.edgekey.net

#Lowe's Checkout
assets.adobedtm.com

#Home Depot Checkout
nexus.ensighten.com

#Mozilla Firefox Tracking Protection
tracking-protection.cdn.mozilla.net

#Playstation 5 "Recently Played Games" and Trophies
telemetry-console.api.playstation.com

#Cannon Printers
gdlp01.c-wss.com

#Reddit
styles.redditmedia.com
www.redditstatic.com
reddit.map.fastly.net
www.redditmedia.com
reddit-uploaded-media.s3-accelerate.amazonaws.com
thumbs.redditmedia.com
redd.it
|reddit.com

#Tracking Packages sent with DPD
tracking.dpd.de

#WhatsApp
wa.me
www/wa/me

#Signal
ud-chat.signal.org
chat.signal.org
storage.signal.org
signal.org
www.signal.org
updates2.signal.org
textsecure-service-whispersystems.org
giphy-proxy-production.whispersystems.org
cdn.signal.org
whispersystems-textsecure-attachments.s3-accelerate.amazonaws.com
d83eunklitikj.cloudfront.net
souqcdn.com
cms.souqcdn.com
api.directory.signal.org
contentproxy.signal.org
turn1.whispersystems.org

#X/Twitter
twitter.com
upload.twitter.com
api.twitter.com
mobile.twitter.com
twimg.com


#Banks

#TBS Mobile
h-sdk.online-metrix.net
check2.tsb.co.uk

#Citizen's Bank
p11.techlab-cdn.com

#OLA Money
logs.juspay.in


#Resturants / Rewards

#Burger King
appboy-images.com
rest.iad-03.braze.com

#Punchh (Farmer Boys, El Pollo Loco, Capriotti's, etc.)
mobileandroidapi.punchh.com

#Rumble
rmbl.ws


#Dutch / The Netherlands websites

#nu.nl (enable videos, tvgids et cetera)
cds.s5x3j6q5.hwcdn.net


#Swedish streaming services

#svtplay (enable continuing where you left off)
analytics.svt.se

```
