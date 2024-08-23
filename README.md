# nostrtok

## Motivation / Background
Video based social media is one of the most popular ways people consume content today. Current content platforms fall victim to what any centralized, advertising based platform faces today–

Advertisers push control over the type of content allowed on the platform
Governments can censor and control content allowed on the platform
Creators are subject to the platform’s decisions and whims and only get a cut of revenue

A decentralized video platform has the potential to disrupt current centralized platform models.

Creators paid directly
Protocol based platform gives no central control over type of content available
Access can be unlimited

Issues to Solve
Video hosting and bandwidth are expensive, which is what drove centralized platforms in the first place
Onboarding as simple as TikTok
Payments

## How it Could Work
### A Creator Uploads a Video
A creator wants to upload a video and potentially make money on it.

They download the nostrtok app, they either enter a Nsec or have a new one generated for them.

The nostrtok app has preset relays and defaults to a global feed.

The creator presses the upload button, they upload their video to a free to start host (first video free).

The nostrtok app signs and sends a note to a nostr relay with a link to the uploaded video and an automatically generated bolt12 invoice.

### Another Nostrtok video viewer sees the video and zaps it
This nostrtok user has linked their lightning wallet with nostr wallet connect and zaps the note from the creator after viewing their video.

The lightning invoice from the original creator’s bolt12 invoice triggers an LSP to open a lightning channel to the creator’s wallet to receive the payment.

The creator is paid for their video from a viewer

### Another Nostrtok viewer reshares the video
Another viewer likes the video so much they reshare it.

Their nostrtok app takes the downloaded video file and uploads it to their own host. The video link is shared out with credit to the original creator, including their bolt12 invoice.

The cost of hosting that video is now shared between the creator and the resharer

_Maybe_– A very small zap revenue share is set up between creator and resharer. Need to examine incentives, but it could help to encourage resharing over downloading and rehosting to steal zaps.


 
## Explanation, Things to Solve
Nostr and current lightning specs enable a very simple onboarding process, distribution, and path to revenue for creators.

The hardest bit to solve here is hosting. Ideally the host is easy to spin up with an API call. I think DWN is what you want here, but could involve some setup process.

Distributed hosting could be accomplished via something like bittorrent. The video link could be a magnet URI, allowing new viewers to pull from a growing pool of hosts.

Users pick what content they host themselves. Getting a cut of zap revenue could help incentivize. A creator could dedicate something like 10% of their zaps to resharers to cover their hosting costs. Hosts could pop up that offer free to start services for a programmatic cut of zap revenue.

Content hosts are still responsible for the content they create or amplify, but the idea is content can be distributed across many hosts, some operated by companies for profit, some run at home by creators themselves. A small rev share cut could encourage a cottage industry of content rehosters.

People hosting bad or illegal content do so directly (opening themselves up to being held responsible if content is illegal), or at the whim of a content host with their own TOS.
