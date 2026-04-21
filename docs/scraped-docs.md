# Trigger.dev — Scraped Documentation

**Source:** https://trigger.dev
**Pages scraped:** 14
**Total characters:** 85529

---

## Overview - Trigger.dev

**URL:** https://trigger.dev/docs/management/overview

Overview - Trigger.dev
Skip to main content
Trigger.dev
home page
Search...
⌘
K
API reference
The Trigger.dev API
API reference
Overview
Authentication
Errors and retries
Auto-pagination
Advanced usage
Tasks API
POST
Trigger
POST
Batch trigger
POST
Trigger task batch
Batches API
POST
Create batch
GET
Retrieve a batch
GET
Retrieve batch results
POST
Stream batch items
Runs API
GET
List runs
GET
Retrieve run
POST
Replay run
POST
Cancel run
POST
Reschedule run
PUT
Update metadata
POST
Add tags to a run
GET
Retrieve run events
GET
Retrieve run trace
GET
Retrieve run result
Queues API
GET
List Queues
GET
Retrieve Queue
POST
Pause or Resume Queue
POST
Override Concurrency Limit
POST
Reset Concurrency Limit
Schedules API
GET
List Schedules
POST
Create Schedule
GET
Retrieve Schedule
PUT
Update Schedule
DEL
Delete Schedule
POST
Deactivate Schedule
POST
Activate Schedule
GET
Get timezones
Env Vars API
GET
List Env Vars
POST
Import Env Vars
POST
Create Env Var
GET
Retrieve Env Var
PUT
Update Env Var
DEL
Delete Env Var
Deployments API
GET
List deployments
GET
Get deployment
GET
Get latest deployment
POST
Promote deployment
Waitpoints API
POST
Create a waitpoint token
GET
List waitpoint tokens
GET
Retrieve a waitpoint token
POST
Complete a waitpoint token
POST
Complete a waitpoint token via HTTP callback
Query API
POST
Execute a query
GET
Get query schema
GET
List dashboards
triggerdotdev/trigger.dev
Trigger.dev
home page
Search...
⌘
K
Ask AI
Search...
Navigation
API reference
Overview
​
Installation
The management API is available through the same
@trigger.dev/sdk
package used in defining and triggering tasks. If you have already installed the package in your project, you can skip this step.
npm
pnpm
yarn
npm
i
@trigger.dev/sdk@latest
​
Usage
All
v3
functionality is provided through the
@trigger.dev/sdk
module. You can import the entire module or individual resources as needed.
import
{ configure
,
runs }
from
"@trigger.dev/sdk"
;
configure
({
// this is the default and if the `TRIGGER_SECRET_KEY` environment variable is set, can omit calling configure
secretKey
:
process
.env[
"TRIGGER_SECRET_KEY"
]
,
});
async
function
main
() {
const
runs
=
await
runs
.list
({
limit
:
10
,
status
:
[
"COMPLETED"
]
,
});
}
main
()
.catch
(
console
.error);
Was this page helpful?
Yes
No
Suggest edits
Raise issue
Authentication
Authenticating with the Trigger.dev management API
Next
⌘
I
On this page
Installation
Usage
Assistant
Responses are generated using AI and may contain mistakes.

---

## Welcome to the Trigger.dev docs - Trigger.dev

**URL:** https://trigger.dev/docs

Welcome to the Trigger.dev docs - Trigger.dev
Skip to main content
Trigger.dev
home page
Search...
⌘
K
Documentation
Resources for Trigger.dev
Getting started
Introduction
Quick start
Manual setup
Video walkthrough
How it works
Limits
Migrating from v3
Fundamentals
Tasks
Triggering
Runs
API keys
Building with AI
Overview
MCP Server
Skills
Agent rules
Writing tasks
Overview
Logging, tracing & metrics
Errors & Retrying
Wait
Concurrency & Queues
Versioning
Machines
Idempotency
Max duration
Heartbeats
Tags
Metadata
Streams
Usage
Context
Priority
Hidden tasks
Configuration
trigger.config.ts
Build extensions
Development
CLI dev command
Deployment
Overview
Environment Variables
CI / GitHub Actions
Preview branches
Atomic deploys
Deployment integrations
Realtime
Overview
How it works
The run object
Realtime auth
React hooks
Backend
CLI
Introduction
Commands
Observability
Query
Dashboards
Using the Dashboard
Run tests
Alerts
Replaying
Bulk actions
Troubleshooting
Common problems
How to reduce your spend
Debugging in VS Code
Upgrading packages
Uptime Status
GitHub Issues
Request a feature
Self-hosting
Overview
Docker compose
Kubernetes
Environment variables
Docker (legacy)
Open source
Contributing
GitHub repo
Changelog
Roadmap
Help
Discord Community
Slack support
Email us
triggerdotdev/trigger.dev
Trigger.dev
home page
Search...
⌘
K
Ask AI
Search...
Navigation
Getting started
Welcome to the Trigger.dev docs
Quick start
Get started with Trigger.dev and run your first task in 3 minutes
Guides, frameworks & examples
Browse our wide range of guides, frameworks and example projects
Building with AI
Learn how to build Trigger.dev projects using AI coding assistants
Video walkthrough
Watch an end-to-end demo of Trigger.dev in 10 minutes
​
What is Trigger.dev?
Trigger.dev is an open source background jobs framework that lets you write reliable workflows in plain async code. Run long-running AI tasks, handle complex background jobs, and build AI agents with built-in queuing, automatic retries, and real-time monitoring. No timeouts, elastic scaling, and zero infrastructure management required.
We provide everything you need to build and manage background tasks: a CLI and SDK for writing tasks in your existing codebase, support for both
regular
and
scheduled
tasks, full observability through our dashboard, and a
Realtime API
with
React hooks
for showing task status in your frontend. You can use
Trigger.dev Cloud
or
self-host
on your own infrastructure.
​
Learn the concepts
Writing tasks
Tasks are the core of Trigger.dev. Learn what they are and how to write them.
Triggering tasks
Learn how to trigger tasks from your codebase.
Runs
Runs are the instances of tasks that are executed. Learn how they work.
API keys
API keys are used to authenticate requests to the Trigger.dev API. Learn how to create and use
them.
​
Explore by feature
Scheduled tasks (cron)
Scheduled tasks are a type of task that is scheduled to run at a specific time.
Realtime API
The Realtime API allows you to trigger tasks and get the status of runs.
React hooks
React hooks are a way to show task status in your frontend.
Waits
Waits are a way to wait for a task to finish before continuing.
Errors and retries
Learn how to handle errors and retries.
Concurrency & Queues
Configure what you want to happen when there is more than one run at a time.
Wait for token (human-in-the-loop)
Pause runs until a token is completed via an approval workflow.
Build extensions
Customize the build process or the resulting bundle and container image.
​
Explore by build extension
Extension
What it does
Docs
prismaExtension
Use Prisma with Trigger.dev
Learn more
pythonExtension
Execute Python scripts in Trigger.dev
Learn more
playwright
Use Playwright with Trigger.dev
Learn more
puppeteer
Use Puppeteer with Trigger.dev
Learn more
lightpanda
Use Lightpanda with Trigger.dev
Learn more
ffmpeg
Use FFmpeg with Trigger.dev
Learn more
aptGet
Install system packages with aptGet
Learn more
additionalFiles
Copy additional files to the build directory
Learn more
additionalPackages
Include additional packages in the build
Learn more
syncEnvVars
Automatically sync environment variables to Trigger.dev
Learn more
esbuildPlugin
Add existing or custom esbuild plugins to your build process
Learn more
emitDecoratorMetadata
Support for the emitDecoratorMetadata TypeScript compiler
Learn more
audioWaveform
Support for Audio Waveform in your project
Learn more
​
Explore by example
FFmpeg
Fal.ai
Puppeteer
LibreOffice
OpenAI
Browserbase
Sentry
Resend
Vercel AI SDK
Sharp
Deepgram
Supabase
DALL•E
Firecrawl
Lightpanda
​
Getting help
We’d love to hear from you or give you a hand getting started. Here are some ways to get in touch with us.
Join our Discord server
Our Discord is the best place to get help with any questions about Trigger.dev.
Follow us on X (Twitter)
Follow us to get the latest updates and news.
Schedule a call
Arrange a call with one of the founders to get help with any questions.
Give us a star on GitHub
Check us out our GitHub repo and give us a star if you like what we’re doing.
Was this page helpful?
Yes
No
Suggest edits
Raise issue
Quick start
Set up Trigger.dev in your existing project in under 3 minutes. Install the SDK, create your first background task, and trigger it from your code.
Next
⌘
I
Assistant
Responses are generated using AI and may contain mistakes.

---

## AI agents overview - Trigger.dev

**URL:** https://trigger.dev/docs/guides/ai-agents

AI agents overview - Trigger.dev
Skip to main content
Trigger.dev
home page
Search...
⌘
K
Guides & examples
A great way to get started
Introduction
Overview
Frameworks
Bun
Next.js
Node.js
Remix
SvelteKit
Guides
AI Agents
Overview
Generate & translate copy
Route a question
Respond & check content
Translate and refine
Verify news article
Claude Agent SDK
Drizzle setup guide
Prisma setup guide
Nango OAuth guide
Sequin database triggers
Supabase
Webhooks
Migration guides
Migrating from Mergent
Migrating from n8n
Use cases
Overview
Data processing & ETL
AI media generation
Media processing
Marketing
Example projects
Anchor Browser web scraper
Batch LLM Evaluator
Claude changelog generator
Claude GitHub wiki
Claude thinking chatbot
Cursor background agent
Human-in-the-loop workflow
Mastra agents with memory
AI meme generator
OpenAI Agents SDK for Typescript playground
Product image generator
Realtime CSV Importer
Realtime image gen with Fal.ai
Smart Spreadsheet
Turborepo monorepo with Prisma
Deep research agent
Vercel AI SDK image generator
Python guides
OpenAI Agents SDK for Python guardrails
Process images
Convert docs to markdown
Headless web crawler
Extract form data from PDFs
Example tasks
DALL·E image generation
Deepgram audio transcription
Fal.ai image to cartoon
Fal.ai with Realtime
FFmpeg video processing
Firecrawl URL crawl
Lightpanda
v4
LibreOffice PDF conversion
OpenAI with retrying
PDF to image
Puppeteer
React to PDF
React Email
Replicate image generation
Resend email sequence
Satori OG Images
Browserbase & Puppeteer
Sentry error tracking
Sharp image processing
Supabase database operations
Supabase Storage upload
Vercel AI SDK
Vercel sync env vars
Community packages
dotenvx
Fatima
Rate limiter
SvelteKit
triggerdotdev/trigger.dev
Trigger.dev
home page
Search...
⌘
K
Ask AI
Search...
Navigation
AI Agents
AI agents overview
​
Example projects using AI agents
Claude changelog generator
Automatically generate professional changelogs from git commits using Claude.
Claude GitHub wiki agent
Generate and maintain GitHub wiki documentation with Claude-powered analysis.
Human-in-the-loop workflow
Create audio summaries of newspaper articles using a human-in-the-loop workflow built with
ReactFlow and Trigger.dev waitpoint tokens.
Mastra agents with memory
Use Mastra to create a weather agent that can collect live weather data and generate clothing
recommendations.
OpenAI Agent Python SDK guardrails
Use the OpenAI Agent SDK to create a guardrails system for your AI agents.
OpenAI Agent TypeScript SDK playground
A playground containing 7 AI agents using the OpenAI Agent SDK for TypeScript with Trigger.dev.
Vercel AI SDK deep research agent
Use the Vercel AI SDK to generate comprehensive PDF reports using a deep research agent.
Smart Spreadsheet
Enrich company data using Exa search and Claude with real-time streaming results.
​
Agent fundamentals
These guides will show you how to set up different types of AI agent workflows with Trigger.dev. The examples take inspiration from Anthropic’s blog post on
building effective agents
.
Prompt chaining
Chain prompts together to generate and translate marketing copy automatically
Routing
Send questions to different AI models based on complexity analysis
Parallelization
Simultaneously check for inappropriate content while responding to customer inquiries
Orchestrator
Coordinate multiple AI workers to verify news article accuracy
Evaluator-optimizer
Translate text and automatically improve quality through feedback loops
Was this page helpful?
Yes
No
Suggest edits
Raise issue
Previous
Generate & translate copy
Create an AI agent workflow that generates and translates copy
Next
⌘
I
On this page
Example projects using AI agents
Agent fundamentals
Assistant
Responses are generated using AI and may contain mistakes.

---

## Docker (legacy) - Trigger.dev

**URL:** https://trigger.dev/docs/open-source-self-hosting

Docker (legacy) - Trigger.dev
Skip to main content
Trigger.dev
home page
Search...
⌘
K
Documentation
Resources for Trigger.dev
Getting started
Introduction
Quick start
Manual setup
Video walkthrough
How it works
Limits
Migrating from v3
Fundamentals
Tasks
Triggering
Runs
API keys
Building with AI
Overview
MCP Server
Skills
Agent rules
Writing tasks
Overview
Logging, tracing & metrics
Errors & Retrying
Wait
Concurrency & Queues
Versioning
Machines
Idempotency
Max duration
Heartbeats
Tags
Metadata
Streams
Usage
Context
Priority
Hidden tasks
Configuration
trigger.config.ts
Build extensions
Development
CLI dev command
Deployment
Overview
Environment Variables
CI / GitHub Actions
Preview branches
Atomic deploys
Deployment integrations
Realtime
Overview
How it works
The run object
Realtime auth
React hooks
Backend
CLI
Introduction
Commands
Observability
Query
Dashboards
Using the Dashboard
Run tests
Alerts
Replaying
Bulk actions
Troubleshooting
Common problems
How to reduce your spend
Debugging in VS Code
Upgrading packages
Uptime Status
GitHub Issues
Request a feature
Self-hosting
Overview
Docker compose
Kubernetes
Environment variables
Docker (legacy)
Open source
Contributing
GitHub repo
Changelog
Roadmap
Help
Discord Community
Slack support
Email us
triggerdotdev/trigger.dev
Trigger.dev
home page
Search...
⌘
K
Ask AI
Search...
Navigation
Self-hosting
Docker (legacy)
This is a legacy guide for self-hosting v3 using Docker, you can find the v4 guide
here
.
Security, scaling, and reliability concerns are not fully addressed here. This guide is meant for evaluation purposes and won’t result in a production-ready deployment.
​
Overview
The self-hosting guide covers two alternative setups. The first option uses a simple setup where you run everything on one server. With the second option, the webapp and worker components are split on two separate machines.
You’re going to need at least one Debian (or derivative) machine with Docker and Docker Compose installed. We’ll also use Ngrok to expose the webapp to the internet.
​
Support
It’s dangerous to go alone! Join the self-hosting channel on our
Discord server
.
​
Caveats
The v3 worker components don’t have ARM support yet.
This guide outlines a quick way to start self-hosting Trigger.dev for evaluation purposes - it won’t result in a production-ready deployment. Security, scaling, and reliability concerns are not fully addressed here.
As self-hosted deployments tend to have unique requirements and configurations, we don’t provide specific advice for securing your deployment, scaling up, or improving reliability.
Should the burden ever get too much, we’d be happy to see you on
Trigger.dev cloud
where we deal with these concerns for you.
Please consider these additional warnings
The
docker checkpoint
command is an experimental feature which may not work as expected. It won’t be enabled by default. Instead, the containers will stay up and their processes frozen. They won’t consume CPU but they
will
consume RAM.
The
docker-provider
does not currently enforce any resource limits. This means your tasks can consume up to the total machine CPU and RAM. Having no limits may be preferable when self-hosting, but can impact the performance of other services.
The worker components (not the tasks!) have direct access to the Docker socket. This means they can run any Docker command. To restrict access, you may want to consider using
Docker Socket Proxy
.
The task containers are running with host networking. This means there is no network isolation between them and the host machine. They will be able to access any networked service on the host.
There is currently no support for adding multiple worker machines, but we’re working on it.
​
Requirements
4 CPU
8 GB RAM
Debian or derivative
Optional: A separate machine for the worker components
You will also need a way to expose the webapp to the internet. This can be done with a reverse proxy, or with a service like Ngrok. We will be using the latter in this guide.
​
Option 1: Single server
This is the simplest setup. You run everything on one server. It’s a good option if you have spare capacity on an existing machine, and have no need to independently scale worker capacity.
​
Server setup
Some very basic steps to get started:
Install Docker
Install Docker Compose
Install Ngrok
On a Debian server, you can run these commands
# add ngrok repo
curl
-s
https://ngrok-agent.s3.amazonaws.com/ngrok.asc
|
\
sudo
tee
/etc/apt/trusted.gpg.d/ngrok.asc
>
/dev/null
&&
\
echo
"deb https://ngrok-agent.s3.amazonaws.com buster main"
|
\
sudo
tee
/etc/apt/sources.list.d/ngrok.list
# add docker repo
curl
-fsSL
https://download.docker.com/linux/debian/gpg
-o
/etc/apt/keyrings/docker.asc
&&
\
sudo
chmod
a+r
/etc/apt/keyrings/docker.asc
&&
\
echo
\
"deb [arch=$(
dpkg
--print-architecture
) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
$(
.
/etc/os-release
&&
echo
"$VERSION_CODENAME") stable"
|
\
sudo
tee
/etc/apt/sources.list.d/docker.list
>
/dev/null
# update and install
sudo
apt-get
update
sudo
apt-get
install
-y
\
docker.io
\
docker-compose-plugin
\
ngrok
​
Trigger.dev setup
Clone the
Trigger.dev docker repository
git
clone
https://github.com/triggerdotdev/docker
cd
docker
Run the start script and follow the prompts
./start.sh
# hint: you can append -d to run in detached mode
​
Manual
Alternatively, you can follow these manual steps after cloning the docker repo:
Create the
.env
file
cp
.env.example
.env
Generate the required secrets
echo
MAGIC_LINK_SECRET=
$(
openssl
rand
-hex
16
)
echo
SESSION_SECRET=
$(
openssl
rand
-hex
16
)
echo
ENCRYPTION_KEY=
$(
openssl
rand
-hex
16
)
echo
PROVIDER_SECRET=
$(
openssl
rand
-hex
32
)
echo
COORDINATOR_SECRET=
$(
openssl
rand
-hex
32
)
Replace the default secrets in the
.env
file with the generated ones
Run docker compose to start the services
.
lib.sh
# source the helper function
docker_compose
-p=trigger
up
​
Tunnelling
You will need to expose the webapp to the internet. You can use Ngrok for this. If you already have a working reverse proxy setup and a domain, you can skip to the last step.
Start Ngrok. You may get prompted to sign up - it’s free.
./tunnel.sh
Copy the domain from the output, for example:
1234-42-42-42-42.ngrok-free.app
Uncomment the
TRIGGER_PROTOCOL
and
TRIGGER_DOMAIN
lines in the
.env
file. Set it to the domain you copied.
TRIGGER_PROTOCOL
=
https
TRIGGER_DOMAIN
=
1234-42-42-42-42.ngrok-free.app
Quit the start script and launch it again, or run this:
./stop.sh
&&
./start.sh
​
Registry setup
If you want to deploy v3 projects, you will need access to a Docker registry. The
CLI deploy
command will push the images, and then the worker machine can pull them when needed. We will use Docker Hub as an example.
Sign up for a free account at
Docker Hub
Edit the
.env
file and add the registry details
DEPLOY_REGISTRY_HOST
=
docker.io
DEPLOY_REGISTRY_NAMESPACE
=<
your_dockerhub_username
>
Log in to Docker Hub both locally and your server. For the split setup, this will be the worker machine. You may want to create an
access token
for this.
docker
login
-u
<
your_dockerhub_usernam
e
>
docker.io
Required on some systems: Run the login command inside the
docker-provider
container so it can pull deployment images to run your tasks.
docker
exec
-ti
\
trigger-docker-provider-1
\
docker
login
-u
<
your_dockerhub_usernam
e
>
docker.io
Restart the services
./stop.sh
&&
./start.sh
You can now deploy v3 projects using the CLI with these flags:
npx trigger.dev@latest deploy --self-hosted --push
​
Option 2: Split services
With this setup, the webapp will run on a different machine than the worker components. This allows independent scaling of your workload capacity.
​
Webapp setup
All steps are the same as for a single server, except for the following:
Startup.
Run the start script with the
webapp
argument
./start.sh
webapp
Tunnelling.
This is now
required
. Please follow the
tunnelling
section.
​
Worker setup
Environment variables.
Copy your
.env
file from the webapp to the worker machine:
# an example using scp
scp
-3
root@
<
webapp_machin
e
>
:docker/.env
root@
<
worker_machin
e
>
:docker/.env
Startup.
Run the start script with the
worker
argument
./start.sh
worker
Tunnelling.
This is
not
required for the worker components.
Registry setup.
Follow the
registry setup
section but run the last command on the worker machine - note the container name is different:
docker
exec
-ti
\
trigger-worker-docker-provider-1
\
docker
login
-u
<
your_dockerhub_usernam
e
>
docker.io
​
Additional features
​
Large payloads
By default, payloads over 512KB will be offloaded to S3-compatible storage. If you don’t provide the required env vars, runs with payloads larger than this will fail.
For example, using Cloudflare R2:
OBJECT_STORE_BASE_URL
=
"https://<bucket>.<account>.r2.cloudflarestorage.com"
OBJECT_STORE_ACCESS_KEY_ID
=
"<r2 access key with read/write access to bucket>"
OBJECT_STORE_SECRET_ACCESS_KEY
=
"<r2 secret key>"
Alternatively, you can increase the threshold:
# size in bytes, example with 5MB threshold
TASK_PAYLOAD_OFFLOAD_THRESHOLD
=
5242880
​
Version locking
There are several reasons to lock the version of your Docker images:
Backwards compatibility.
We try our best to maintain compatibility with older CLI versions, but it’s not always possible. If you don’t want to update your CLI, you can lock your Docker images to that specific version.
Ensuring full feature support.
Sometimes, new CLI releases will also require new or updated platform features. Running unlocked images can make any issues difficult to debug. Using a specific tag can help here as well.
By default, the images will point at the latest versioned release via the
v3
tag. You can override this by specifying a different tag in your
.env
file. For example:
TRIGGER_IMAGE_TAG
=
v3.0.4
​
Auth options
By default, magic link auth is the only login option. If the
EMAIL_TRANSPORT
env var is not set, the magic links will be logged by the webapp container and not sent via email.
Depending on your choice of mail provider/transport, you will want to configure a set of variables like one of the following:
Resend:
EMAIL_TRANSPORT
=
resend
FROM_EMAIL
=
REPLY_TO_EMAIL
=
RESEND_API_KEY
=<
your_resend_api_key
>
SMTP
Note that setting
SMTP_SECURE=false
does
not
mean the email is sent insecurely.
This simply means that the connection is secured using the modern STARTTLS protocol command instead of implicit TLS.
You should only set this to true when the SMTP server host directs you to do so (generally when using port 465)
EMAIL_TRANSPORT
=
smtp
FROM_EMAIL
=
REPLY_TO_EMAIL
=
SMTP_HOST
=<
your_smtp_server
>
SMTP_PORT
=
587
SMTP_SECURE
=
false
SMTP_USER
=<
your_smtp_username
>
SMTP_PASSWORD
=<
your_smtp_password
>
AWS Simple Email Service
Credentials are to be supplied as with any other program using the AWS SDK.
In this scenario, you would likely either supply the additional environment variables
AWS_REGION
,
AWS_ACCESS_KEY_ID
and
AWS_SECRET_ACCESS_KEY
or, when running on AWS, use credentials supplied by the EC2 IMDS.
EMAIL_TRANSPORT
=
aws-ses
FROM_EMAIL
=
REPLY_TO_EMAIL
=
All email addresses can sign up and log in this way. If you would like to restrict this, you can use the
WHITELISTED_EMAILS
env var. For example:
# every email that does not match this regex will be rejected
WHITELISTED_EMAILS
=
"^(authorized@yahoo\.com|authorized@gmail\.com)$"
It’s currently impossible to restrict GitHub OAuth logins by account name or email like above, so this method is
not recommended
for self-hosted instances. It’s also very easy to lock yourself out of your own instance.
Only enable GitHub auth if you understand the risks! We strongly advise you against this.
Your GitHub OAuth app needs a callback URL
https://<your_domain>/auth/github/callback
and you will have to set the following env vars:
AUTH_GITHUB_CLIENT_ID
=<
your_client_id
>
AUTH_GITHUB_CLIENT_SECRET
=<
your_client_secret
>
​
Checkpoint support
This requires an
experimental Docker feature
. Successfully checkpointing a task today, does not
mean you will be able to restore it tomorrow. Your data may be lost. You’ve been warned!
Checkpointing allows you to save the state of a running container to disk and restore it later. This can be useful for
long-running tasks that need to be paused and resumed without losing state. Think fan-out and fan-in, or long waits in email campaigns.
The checkpoints will be pushed to the same registry as the deployed images. Please see the
registry setup
section for more information.
​
Requirements
Debian,
NOT
a derivative like Ubuntu
Additional storage space for the checkpointed containers
​
Setup
Underneath the hood this uses Checkpoint and Restore in Userspace, or
CRIU
in short. We’ll have to do a few things to get this working:
Install CRIU
sudo
apt-get
update
sudo
apt-get
install
criu
Tweak the config so we can successfully checkpoint our workloads
mkdir
-p
/etc/criu

[SCRAPER NOTE: This page was truncated by the scraper due to length. Content continues on the live page.]

---

## AI agents | Trigger.dev

**URL:** https://trigger.dev/product/ai-agents

AI agents | Trigger.dev
Drop-in AI agent infrastructure
Focus on building intelligent AI agents, not wrestling with servers. Get the reliability, control, and observability required to deploy invincible AI agents that actually work in production.
Get started now
We run parallel AI tasks for proposal generation and compliance mapping across 10,000+ government sources. Trigger.dev handles the orchestration.
Conner Aldrich
GovSignals
The Trigger.dev developer experience is unparalleled for building durable agents. Queues, streaming, retries, logging and more, all with just a few lines of code.
Justin Sun
Capy
Our platform uses AI agents to gather compliance evidence by querying various API endpoints using MCPs, with browser-based automation as a fallback.
Lewis Carhart
Comp AI
Agents that live in your codebase
Break less things with totally type-safe agents
Our TypeScript SDK provides end-to-end type safety for your AI agents. Define your tasks with Zod schemas and automatically convert them to type-safe tools for AI SDK. And our atomic versioning ensures that you can safely update your agents without breaking changes.
Built on strong foundations
The 6 pillars of building agents
Long-running without timeouts
Execute your tasks with absolutely no timeouts, unlike AWS Lambda, Vercel, and other serverless platforms.
Durability, retries & queues
Build rock solid agents and AI applications using our durable tasks, retries, queues and idempotency.
True runtime freedom
Customize your deployed tasks with system packages – run browsers, Python scripts, FFmpeg and more.
Human-in-the-loop
Programmatically pause your tasks until a human can approve, reject or give feedback.
Realtime apps & streaming
Move your background jobs to the foreground by subscribing to runs or streaming AI responses to your app.
Observability & monitoring
Each run has full tracing and logs. Configure error alerts to catch bugs fast. Monitor performance with metrics.
Library, model, and framework agnostic
Plays well with others
It is easy to build and adapt your workflows using the latest libraries, models or frameworks as soon as they're released.
AI SDK
A TypeScript-first library for building AI applications with multi-provider support, streaming responses, tool usage, web search.
Agents SDK (JS/TS)
Build agentic AI applications with function calling, streaming, guardrails, tool usage, and multi-step reasoning.
Agents SDK (Python)
With the Trigger.dev Python extension your can use Python libraries like OpenAI's Agents SDK, Langchain, and more.
Use cases
AI agents in action
From basic prompt chains to sophisticated multi-step workflows, see how developers are building production AI agents. These examples showcase the patterns and techniques that work in real-world applications. All of these examples are open source and have full documentation for you to learn from.
Prompt chaining
Generate and translate
Routing
Route through LLMs
Evaluator-optimizer
Translate and refine
Orchestrator
Verify news articles
Parallelization
Moderate content
Autonomous agent
Deep research
Modern agent infrastructure
The building blocks for agents
Write agents in regular code
Build AI agents using familiar programming models in native Javascript / Typescript.
Learn more
Agent observability
Monitor every aspect of your agents' performance with comprehensive logging and visualization tools.
Learn more
Human-in-the-loop
Pause for human approval at critical decision points, resume on command.
Learn more
Structured inputs / outputs
Define precise data schemas for your agents using SchemaTask with runtime validation to ensure consistent and predictable interactions.
Learn more
Input Streams
Send cancel signals, approvals, or any typed data into running agents from your backend or frontend.
Learn more
Machines
Configure the number of vCPUs and GBs of RAM you want the task to use.
Learn more
Autoscaling
Elastic infrastructure which auto-scales resources up or down as needed.
Learn more
Build extensions
Control the deployed packages using our build extensions (control browsers, run Python, use FFmpeg, etc).
Learn more
Realtime run status updates
Subscribe to runs for real-time updates. Stream AI responses directly to users with built-in observability.
Learn more
Agent concurrency controls
Control the concurrency of your tasks from one at a time, to parallel, to per-tenant queuing using concurrency keys.
Learn more
Versioning
Deploy new code without affecting running tasks — atomic version rollouts.
Learn more
Sandboxing
(coming soon)
Generate code at runtime and execute it in secure cloud sandboxes.
Ready to start building agents?
Build and deploy your first AI task in 3 minutes.
Get started now

---

## Trigger.dev Realtime | Trigger.dev

**URL:** https://trigger.dev/product/realtime

Trigger.dev Realtime | Trigger.dev
Realtime: Move your background jobs to the foreground
Subscribe to your runs and receive updates anywhere in your frontend or backend, in real-time. Stream AI responses to your users from your runs, with full observability built-in.
Real-time task progress
Display task status and metadata anywhere on your frontend
Get the live status of your runs (in progress, completed, failed) with detailed outputs, and use metadata to provide detailed context for your users.
Trigger.dev Realtime docs
Update your UI in real-time
as tasks progress
Working with AI
Pipe LLM streams straight to your users
Forward streams through the Realtime API to provide real-time updates to your users from any AI providers. Create AI agents with tools and context from your runs.
Realtime Streams docs
Stream AI responses to your users
from your runs
Using our Realtime React hooks
We provide a set of React hooks to securely interact with the Trigger API from your React app. Subscribe to your runs, trigger tasks and more.
useRealtimeRun
Trigger a task and subscribe to a run by it’s ID.
useRealtimeRunsWithTag
Subscribe to multiple runs with a specific tag.
useRealtimeBatch
Subscribe to a batch of runs by its the batch ID.
useRealtimeRunWithStreams
Subscribe to a run by its ID and also receive any streams that are emitted by the task.
publicToken
Configure the Public Access Token scopes to authenticate requests.
"use client"
;
// This is needed for Next.js App Router or other RSC frameworks
import
{
useRealtimeRun
}
from
"@trigger.dev/react-hooks"
;
export
function
MyComponent
(
{
runId
,
publicAccessToken
,
}
:
{
runId
:
string
;
publicAccessToken
:
string
;
}
)
{
const
{
run
,
error
}
=
useRealtimeRun
(
runId
,
{
accessToken
:
publicAccessToken
,
}
)
;
if
(
error
)
return
<
div
>
Error
:
{
error
.
message
}
<
/
div
>
;
return
<
div
>
Run
:
{
run
.
id
}
<
/
div
>
;
}
Ready to start building?
Build and deploy your first task in 3 minutes.
Get started now

---

## Cron schedules | Trigger.dev

**URL:** https://trigger.dev/product/scheduled-tasks

Cron schedules | Trigger.dev
Build reliable cron schedules
Use schedules for recurring tasks, like a cron job every 5 minutes, a task that runs at 9.30am every other Monday, or even a task that runs just once a year.
Get started now
Schedules docs
Add schedules to your tasks either in code, or using our dashboard. These can be either
simple
or
multi-tenant
, depending on your needs.
Declarative schedules
Add schedules to your tasks which sync when you run dev or deploy
We recommend declarative tasks for internal jobs. They live directly in your code so are version controlled in Git.
Declarative schedules docs
export
const
secondScheduledTask
=
schedules
.
task
(
{
id
:
"second-scheduled-task"
,
cron
:
{
// 5am every day Tokyo time
pattern
:
"0 5 * * *"
,
timezone
:
"Asia/Tokyo"
,
}
,
run
:
async
(
payload
)
=>
{
}
,
}
)
;
If you specify a timezone we'll automatically adjust for Daylight Saving Time for you.
Imperative schedules in the dashboard
Attach schedules to your tasks, using the dashboard
Create, activate, disable, edit and delete schedules in the dashboard without having to deploy any new code.
Imperative schedules dashboard docs
Use AI and natural language to easily create cron expressions for your schedules. No more having to manually figure out complicated cron syntax.
Imperative schedules in the SDK
Attach schedules to your tasks using our SDK
Allows you to easily add schedules for your tenants using
externalId
.
Imperative schedules in the SDK docs
const
createdSchedule
=
await
schedules
.
create
(
{
// The id of the scheduled task you want to attach to.
task
:
firstScheduledTask
.
id
,
// The schedule in cron format.
cron
:
"0 0 * * *"
,
// This is required, it prevents you from creating duplicate schedules.
// It will update the schedule if it already exists.
deduplicationKey
:
"my-deduplication-key"
,
}
)
;
Schedules are instantly created when schedules.create() is run. This is a powerful way of creating multi-tenant schedules for your users.
As someone who can never remember the right format for a cron job, I love the option to enter it in plain English and get it generated for me.
DomNeuner
Multi-tenant schedules
Advanced dynamic schedules for your individual users
Multi-tenant schedules allow you to configure dynamic schedules depending on your user's behaviour with your product or service.
Multi-tenant schedules docs
Example schedules
Sync Airtable to the database
Periodically sync modified records from an Airtable table to a database.
Post GIF to Slack on a schedule
Select a random GIF from Giphy and post it to Slack every 2 minutes.
Generate text daily, using OpenAI
Create a motivational message using AI; every morning at 5am, Tokyo time.
import
{
schedules
}
from
"@trigger.dev/sdk"
export
const
syncAirtable
=
schedules
.
task
(
{
id
:
"sync-airtable"
,
run
:
async
(
{
timestamp
,
lastTimestamp
}
)
=>
{
await
airtable
<
StoreItems
>
(
"Store items"
)
.
select
(
{
filterByFormula
:
encodeURIComponent
(
`
AND(LAST_MODIFIED_TIME() >=
${
lastTimestamp
}
,
LAST_MODIFIED_TIME() <=
${
timestamp
}
)
`
)
,
}
)
.
eachPage
(
async
(
records
,
fetchNextPage
)
=>
{
for
(
const
record
of
records
)
{
const
result
=
await
processItem
(
record
.
fields
)
;
await
db
.
storeItems
.
upsert
(
result
.
id
,
result
)
;
}
// Repeat for the next page
fetchNextPage
(
)
;
}
)
;
}
,
}
)
;
Ready to start building?
Build and deploy your first task in 3 minutes.
Get started now

---

## https://trigger.dev/product/concurrency

**URL:** https://trigger.dev/product/concurrency

> **Error:** Client error '404 Not Found' for url 'https://trigger.dev/product/concurrency'
For more information check: https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/404


---

## Cloud Pricing | Trigger.dev

**URL:** https://trigger.dev/pricing

Cloud Pricing | Trigger.dev
Simple pricing, built for growth
Begin for free, invite your team, and scale without limits.
Free
$0
/month
$
5
free monthly usage
Get started
20
concurrent runs
Unlimited
tasks
5
team members
Dev and Prod
environments
Preview
branches
Custom dashboards
10
schedules
1
day log retention
1
day
query period
Community support
1
alert destination
10
concurrent Realtime connections
Hobby
$10
/month
$
10
monthly usage included
Get started
50
concurrent runs
Unlimited
tasks
5
team members
Dev, Preview and Prod
environments
5
preview
branches
1
custom
dashboard
100
schedules
7
day log retention
7
days
query period
Community support
3
alert destinations
50
concurrent Realtime connections
Pro
$50
/month
$
50
monthly usage included
Get started
200
+
concurrent runs
Then $10/month per 50
Unlimited
tasks
25
+
team members
Then $20/month per seat
Dev, Preview and Prod
environments
20
+
preview
branches
Then $10/month per branch
5
+
custom
dashboards
Then $10/month per dashboard
1000
+
schedules
Then $10/month per 1,000
30
day log retention
30
days
query period
Dedicated Slack support
100
+
alert destinations
500
+
concurrent Realtime connections
Then $10/month per 1,000
Enterprise
A custom plan tailored to your requirements
All Pro plan features +
Custom log retention
Priority support
Role-based access control
SOC 2 report
SSO
Contact us
Compute pricing
Per sec
Per hour
Machine
vCPU
GB RAM
Cost/
sec
Micro
0.25
0.25
$0.0000169
Small 1x
Default
0.5
0.5
$0.0000338
Small 2x
1
1
$0.0000675
Medium 1x
1
2
$0.0000850
Medium 2x
2
4
$0.0001700
Large 1x
4
8
$0.0003400
Large 2x
8
16
$0.0006800
Tasks are executed on our managed workers. You are only charged when your tasks are executing.
Run pricing
Cost/run invocation
$
0.000025
($
0.25
per 10,000 runs)
Every run that starts executing on our managed workers is charged an invocation cost in addition to compute costs. Runs in the DEV environment are not charged for.
Frequently asked questions
What is a task?
Tasks are functions that can run for a long time and provide strong resilience to failure. They run on our servers so there are no timeouts and no infrastructure to manage. You can read more about how they work in
our docs
.
Can I self-host Trigger.dev?
Absolutely. We have a self hosting guide
right here
.
How long can a task run for?
Tasks can run for as long as you need, with no timeouts.
Where are my tasks run?
In order to provide reliable tasks with no timeouts, we host your task code on our servers and run it on our infrastructure. Your tasks are added to
/trigger
folders and code inside these is bundled and deployed together. Of course you can
self-host
everything if you prefer.
How do I estimate my usage?
Multiply per second machine price by the seconds your run will take. Add the per run invocation cost and multiply by your run count.
A 10s task that does 100 runs per day on the small-1x machine:
1 run = (10s × $0.0000338) + $0.000025 = $0.000363
1 day = 100 × $0.000363 = $0.0363
1 month = $0.0363 × 30 = $1.09
How does usage work?
We charge for usage in 2 ways: the number of seconds of compute your tasks execute for, and the number of runs you do. The
compute cost
depends on the machine you've chosen.
When triggering and waiting for subtasks, the parent is checkpointed and while waiting does not count towards compute usage. When waiting for a time period (wait.for or wait.until), if the wait is longer than 5 seconds we checkpoint and it does not count towards compute usage.
Are there rate limits?
Yes. The free plan is limited to 60 API requests per minute while paid plans are limited to 1,500 API requests per minute. You can trigger more tasks than this by using
batchTrigger()
.
Can I get more concurrency?
Yes. Concurrency is limited on our Free plan but you can increase your concurrency limit by upgrading to a paid plan. If your tasks require more than the Pro plan limit (
200
), you can purchase bundles of
50
for
$10
per month.
Do tasks waiting to execute count towards my concurrency limit?
No. Concurrency limits in Trigger.dev only apply when code is executing. Our built-in
wait
functions snapshot the process and restore it later, meaning you don't pay for time spent waiting. This approach allows you to efficiently manage long-running tasks, such as multi-day email marketing flows, without unnecessarily consuming your concurrency limits or incurring costs during idle periods.
Can I run Trigger.dev locally?
Yes. Using our CLI you develop your tasks locally with hot reloading.
What frameworks does Trigger.dev support?
Trigger.dev is framework agnostic so it works with most JavaScript frameworks. We have created
guides for popular frameworks
which provide a great way to get started.
Can I build complex tasks?
Yes. There’s no limit to the complexity of tasks you can create. Tasks are created in code so you can write conditional, looping, branching or time delayed logic using normal async code.
Can I use version control or roll-backs?
Yes. You create tasks directly in your own code so it’s version controlled with everything else. You can also rollback to previous deploys in the dashboard.
How long does it take to code a task?
A simple task triggering using APIs will take about 5 minutes to create.
Can I use any API I need?
Yes. You can use any API either by using their SDK or through web requests using fetch or your preferred alternative.
Is Trigger.dev open source?
Yes. Trigger.dev is open source using the Apache 2.0 license. We are committed to open source software and working with
our community
to build a great product.
Ready to start building?
Build and deploy your first task in 3 mins with no timeouts and no infrastructure to manage.
Get started for free
Enterprise
Custom plans and support for your enterprise needs.
Contact us
Self-host
Trigger.dev is open source and self-hostable.
Self-hosting docs

---

## Blog | Trigger.dev

**URL:** https://trigger.dev/blog

Blog | Trigger.dev
Blog
All
Articles
Customer Stories
Launch Weeks
We ditched worktrees for Claude Code. Here's what we use instead
Git worktrees solve code isolation but create infrastructure nightmares. We teach Claude Code to use GitButler's CLI directly, splitting one session's work across multiple branches without duplicating databases, Redis, or dev servers.
Article
•
April 16
Why we replaced Node.js with Bun for 5x throughput
How we took our warm start service from 2,099 req/s on Node + SQLite to 10,700 req/s on a compiled Bun binary, and found a subtle memory leak that only exists in Bun's HTTP model.
Article
•
March 27
10 Claude Code Tips You Didn't Know
Skills teach AI agents how to do specific tasks consistently. Learn how they work, what's inside them, and how agents discover and load them.
Article
•
March 12
How we give every user SQL access to a shared ClickHouse cluster
A deep dive into TRQL — the SQL-like language behind Query. How we parse, validate, and compile queries to secure, tenant-safe ClickHouse SQL.
Article
•
March 5
Skills: teaching AI agents to act consistently
Skills teach AI agents how to do specific tasks consistently. Learn how they work, what's inside them, and how agents discover and load them.
Article
•
February 4
How Tierly builds AI-powered pricing intelligence using Trigger.dev
Gerasimos Plegas, Founder at Tierly, shares how they orchestrate complex multi-step AI workflows for competitive pricing analysis using Trigger.dev.
Customer story
•
January 29
Trigger.dev raises $16M Series A
We've raised a $16M Series A led by Standard Capital, with participation from Y Combinator.
Article
•
December 17
How GovSignals is solving government procurement using Trigger.dev
Conner Aldrich, Co-Founder & CTO at GovSignals, shares how his team uses Trigger.dev to power large-scale AI ingestion, high-compute proposal generation, and a dual-deployment model spanning both Trigger cloud and a fully self-hosted, FedRAMP High environment.
Customer story
•
December 11
OTel incident post-mortem
Between November 28 and December 1, 2025, we experienced intermittent failures ingesting trace data into ClickHouse. Here's what happened, why partition key design matters, and how we fixed it.
Post mortem
•
December 2
How we got hit by Shai-Hulud: A complete post-mortem
On November 25th, one of our engineers was compromised by the Shai-Hulud npm supply chain worm. Here's what happened, how we responded, and what we've changed.
Post mortem
•
November 28
Accelerating global logistics workflows using AI copilots
Karl Kaiser, Engineer at Pallet, shares how his team uses Trigger.dev to power their logistics AI copilot, automating the exchange of shipment and transport data between multiple systems in real-time.
Customer story
•
November 13
How we built a kanban-style triage agent for managing coding agents
Justin Sun, Co-founder and CTO of Capy, explains how they use Trigger.dev's workflow engine to run an intelligent triage agent that coordinates many concurrent coding agents in completing end-to-end engineering tasks.
Customer story
•
October 7
Our roadmap for the next 3 months and beyond
After shipping v4 GA, we're focusing on making Trigger.dev the best platform for AI agents. Here's our 3-month+ roadmap: GitHub and Vercel integrations, sub-500ms MicroVM cold starts, improved logging with ClickHouse, an Agent Toolkit, and advanced metrics.
Article
•
September 4
Powering HeroUI Chat's complex deployment pipeline with Trigger.dev
Junior Garcia, founder of HeroUI, explains how Trigger.dev powers the complex deployment pipeline for HeroUI Chat, their AI-powered platform that lets anyone build applications using atomic React components.
Customer story
•
August 29
Official MCP server & agent rules
We've created an official MCP server and agent rules for Trigger.dev that makes getting setup, developing, and debugging your tasks a breeze.
Launch week
•
August 22
4x concurrency, static IPs and multi-region workers powered by AWS
Get 4x more concurrency on paid plans and static IPs with our new AWS regions, starting with us-east-1 and eu-central-1.
Launch week
•
August 21
Bulk actions
Bulk cancel and replay any number of runs using filters.
Launch week
•
August 20
Preview branches
Create isolated environments for each of your git branches.
Launch week
•
August 19
Trigger.dev v4 GA
This is our most significant performance and developer experience upgrade yet, built on our new Run Engine.
Launch week
•
August 18
How we built a real-time service that handles 20,000 updates per second
We process 20,000 run updates per second and 500GB of data daily using Postgres replication slots and ElectricSQL. Here's why we chose this over WebSockets and how we solved the hard problems of authentication, rate limiting, and caching.
Article
•
July 17
How Magic Patterns migrated 200k monthly jobs to Trigger.dev in one day
Alex Danilowicz, Co-founder of Magic Patterns, shares why they migrated their critical background jobs to Trigger.dev from their unreliable self-hosted solution.
Customer story
•
July 8
Self-hosting Trigger.dev v4 using Kubernetes
You can now self-host Trigger.dev v4 using Kubernetes. This adds to the existing Docker option.
Article
•
June 26
Self-hosting Trigger.dev v4 using Docker
You can now self-host Trigger.dev v4 using Docker. This is a big step towards making Trigger.dev more accessible to everyone.
Article
•
June 19
Automating security compliance using AI agents
Lewis Carhart, Founder at Comp AI, shares how they use Trigger.dev to automate evidence collection at scale, powering their open source, AI-driven compliance platform.
Customer story
•
May 27
Icon: revolutionizing video ad creation with Trigger.dev
Caleb Tan, Founding Engineer at Icon, shares how they use Trigger.dev to process thousands of videos concurrently, powering their AI-driven ad creation platform that allows global brands to generate full video ads in minutes.
Customer story
•
April 15
Trigger.dev v4 beta
Today we're excited to launch our v4 beta, that includes Run Engine 2. There are significant performance improvements like warm starts, a totally revamped dashboard, human in the loop tokens, and more.
Article
•
April 9
How to write great Cursor Rules
What we learned writing a Cursor Rules file for Trigger.dev tasks, and 10 tips for writing your own
Article
•
March 27
How Trigger.dev powers Huntr's internal AI agents
Sam Wright, Head of Operations and Partnerships at Huntr, explains how they use Trigger.dev to build AI agents for content generation and internal tooling.
Customer story
•
March 4
How MagicSchool AI develops insights using Trigger.dev
Ben Duggan, Staff Software Engineer at MagicSchool AI, shares how they use Trigger.dev and Vercel's AI SDK to extract insights from millions of student interactions.
Customer story
•
February 12
Building effective AI agents with Trigger.dev
Learn how to build AI agents with Trigger.dev, and how they can help you build more resilient systems.
Article
•
February 6
Midday's Automated Bank Synchronization, powered by Trigger.dev
Pontus Abrahamsson, CEO and co-founder of Midday, deep dives into how they use Trigger.dev to reliably sync bank transactions for their 11,500+ customers.
Customer story
•
January 15
Everything we launched during launchweek[0]
A recap of all the new features we announced during our first launch week.
Launch week
•
December 9
Run Engine 2.0 (alpha)
Warm starts, multi-region workers, self-hosted workers, and new waitpoints.
Launch week
•
December 6
Batch processing
A bunch of improvements to our batch processing system, including new limits and dashboard visibility.
Launch week
•
December 5
Trigger from the frontend
Trigger.dev now supports triggering tasks from the frontend.
Launch week
•
December 4
Build extensions
Install system packages, like FFmpeg and Puppeteer, and modify the build process.
Launch week
•
December 3
Realtime goes GA
Keep your users updated with real-time task progress. Now with LLM streaming support and increased limits.
Launch week
•
December 2
How NUMI uses Trigger.dev to build resilient systems
Agree Ahmed, CEO of NUMI, shares his story of how they have re-architected their code to use Trigger.dev, and how it has changed the way they think about building complex distributed systems.
Customer story
•
November 27
Real-time PDF conversion with Trigger.dev: Papermark's success story
Marc Seitz, co-founder of Papermark, runs through how they have used Trigger.dev to build a real-time PDF conversion service, with thousands of conversions successfully processed per month.
Customer story
•
October 30
How to scrape a website using Browserbase, Puppeteer, OpenAI and Trigger.dev
Learn how to scrape the top 3 articles from Hacker News and email yourself a summary every weekday at 9AM.
Article
•
October 23
Trigger anything from a database change using Supabase with Trigger.dev
Learn how to use Trigger.dev with Supabase to create event-driven workflows. We'll cover triggering tasks from Edge Functions, performing database operations, and building a video processing pipeline with AI transcription.
Article
•
October 17
From beta to 3.0: Trigger.dev v3 reaches GA
Trigger.dev v3 is now out of beta and at v3.0.0. This release includes a new CLI, a revamped build system, and more.
Article
•
September 17
How we stopped xmin horizon blocking Postgres vacuuming: a deepdive
We encountered an issue with xmin horizon blocking Postgres vacuuming, causing system slowdowns. Learn about our troubleshooting process, the solution we implemented, and our steps to prevent similar incidents in the future.
Article
•
August 16
Trigger.dev v2 end-of-life and how to upgrade to v3
Trigger.dev v2 will reach end-of-life on January 31st 2025. Here's what you need to know and how to migrate to v3.
Article
•
August 5
Trigger.dev v3 is now open to everyone
Today, I'm excited to announce that Trigger.dev v3 is now open to everyone. No more waitlist!
Article
•
July 12
How we tamed Node.js event loop lag: a deepdive
We recently experienced some service degradation and downtime due to event loop lag in our Node.js service. Here's how we diagnosed and fixed the issue.
Article
•
June 28
Trigger.dev v3 Developer Preview is now available
Today you can get early access to v3. No timeouts, easy reliability and a new dashboard for finding and fixing bugs.
Article
•
March 25
Trigger.dev v3: Durable Serverless functions. No timeouts.
Write regular code and get durability with no timeouts. This means writing long-running tasks is far easier than before.
Article
•
January 19
Trigger.dev raises $3M
Trigger.dev, the open source background jobs framework, has today announced a $3M seed round.
Article
•
August 25
Ship something amazing today
Deploy and scale your projects with Trigger.dev.
Get started now

---

## Trigger.dev

**URL:** https://trigger.dev/discord

Trigger.dev
You need to enable JavaScript to run this app.

---

## Trigger.dev vs Temporal | Trigger.dev

**URL:** https://trigger.dev/vs/temporal

Trigger.dev vs Temporal | Trigger.dev
Updated
March 2026
Trigger.dev vs Temporal
Long-running workflows need to survive crashes and restarts. Temporal solves this with deterministic replay across seven languages, proven at Netflix-scale with advanced workflow primitives like Signals and Queries. Trigger.dev uses checkpoint-resume to run normal TypeScript with no determinism constraints, processing millions of tasks for thousands of teams on managed infrastructure. Choose Temporal for polyglot enterprise orchestration. Choose Trigger.dev for TypeScript teams that want to ship fast without managing workers.
What is
Trigger.dev
?
Trigger.dev
is a managed compute platform for building AI agents and workflows in TypeScript. Your code runs as normal TypeScript with no determinism constraints and no execution timeout. It includes built-in retries, queues, scheduling, and OpenTelemetry observability with custom dashboards and a SQL-style query language. Tasks can stream data to your frontend in real-time, receive typed input while running, and pause indefinitely for human approval or external events. Thousands of engineering teams run production workloads on it, processing millions of runs.
What is
Temporal
?
Temporal
is a durable execution platform that guarantees your code runs to completion through crashes and outages using event-sourced deterministic replay. It has official SDKs for Go, Java, Python, TypeScript, .NET, PHP, and Ruby, and is used in production by Netflix, OpenAI, Stripe, and JPMorgan Chase. Temporal Cloud has processed over 9.1 trillion lifetime actions.
Feature deep-dive
How does developer experience compare?
Temporal requires you to understand Workflows, Activities, Workers, Task Queues, and Namespaces before you ship. Trigger.dev starts with tasks; queues, workers, and environments are managed for you.
Feature
Trigger.dev
Temporal
Minimum building blocks
Tasks
Workflows + Activities
Execution
Workers (managed or self-hosted)
Workers (self-hosted)
Routing
Queues
Task Queues
Isolation
Projects + Environments
Namespaces
Code constraints
None
Deterministic workflows required
Boilerplate
Minimal: just the task function
Activity stubs, worker setup, workflow registration
Error debugging
OpenTelemetry traces, TRQL dashboards, AI assistant, alerting
Event history, replay debugging, web UI, Grafana integration
Type safety
Full TypeScript types
Full TypeScript types (with proxy indirection)
Primary language
TypeScript-native
Go, Java, Python, TypeScript, .NET, PHP, Ruby
Production CLI
login
,
init
,
dev
,
deploy
workflow
,
batch
,
schedule
,
operator
,
task-queue
Onboarding
init
into your project or a blank folder
Tutorials + sample apps for each SDK
Versioning
Deploy new code, new runs use it. No patching needed
Workflow versioning / patching for in-flight deterministic code
Child tasks
triggerAndWait
/
batchTriggerAndWait
Child workflows with parent-close policies
AI coding tools
MCP server (docs, metrics, write tasks, trigger, monitor, deploy), agent rules, skills, llms.txt
MCP server (workflow lifecycle, batch ops, schedules, event history)
Local development
Hot reload, requires internet
Fully offline dev server
Temporal splits work across Workflows, Activities, Workers, Task Queues, and Namespaces, each unlocking patterns like Signals, Queries, and child workflows. Trigger.dev has one concept:
tasks
. Built-in retries, queues with concurrency keys, scheduled tasks, batch triggering, a Realtime API with React hooks, and OpenTelemetry tracing. Run
npx trigger.dev@latest init
and you're writing tasks in minutes.
No determinism constraints means deploys are simple: new runs use the new version, in-progress runs finish on theirs. Temporal requires explicit versioning when workflow logic changes. Tasks can spawn other tasks and wait for results with
triggerAndWait
. Trigger.dev also ships an
MCP server
, agent rules, and skills for Claude Code, Cursor, Windsurf, and more. Temporal has an MCP server covering workflow lifecycle, batch operations, schedules, and event history.
How does the build and deploy pipeline compare?
Trigger.dev deploys with a single command and manages build dependencies through config. Temporal workers are your build pipeline to own.
Feature
Trigger.dev
Temporal
Build customization
Build extensions (Prisma, FFmpeg, Playwright, Python, more) or write your own
Manage your own Dockerfile
Deploy integrations
GitHub + Vercel: auto-deploy on push, env var sync
Manage your own CI/CD pipeline
Environments
Production, Staging, Preview (per-branch), Development
Namespaces (manual setup)
Build extensions
add system-level dependencies (Prisma, FFmpeg, Playwright, Python, system packages) with a config line, and you can create custom extensions for anything not covered. The
GitHub integration
auto-deploys on every push, and the
Vercel integration
syncs environment variables and supports atomic deploys. Trigger.dev includes built-in production, staging, and development environments, plus
preview branches
that create isolated environments per PR with their own API key, env vars, and schedules, auto-archived when the PR merges. Temporal uses namespaces, but environment management is manual.
How does durability work in each platform?
Both guarantee your code survives crashes and restarts, but Temporal replays events from scratch while Trigger.dev restores memory snapshots.
Feature
Trigger.dev
Temporal
Durability model
Checkpoint-resume snapshots
Event-sourcing with deterministic replay
Determinism required
No
Yes: no
Date.now()
,
Math.random()
, or direct I/O
Recovery mechanism
Restore from checkpoint
Replay from event history
Long-running workflows
Checkpoints grow with process memory
continue-as-new
resets event history
Temporal uses
event-sourcing with deterministic replay
. Every workflow action is recorded as an event, and on recovery the workflow replays from the start, skipping completed activities. This gives Temporal a complete, replayable audit trail and powers advanced patterns like
continue-as-new
for extremely long-running workflows. Trigger.dev uses
checkpoint-resume
instead. When your task reaches a wait point, the platform snapshots your task's state and restores it later. The tradeoff is losing the replayable event history, but your code runs as plain TypeScript with no determinism rules. There are no limits on execution time, you don't need to do workarounds like "continue-as-new."
How do AI agent capabilities compare?
Temporal has deep Python AI integration through the OpenAI Agents SDK and multi-language agent orchestration. Trigger.dev is purpose-built for TypeScript AI agents with real-time streaming, human-in-the-loop, and no timeout.
Feature
Trigger.dev
Temporal
AI framework support
Any TS framework (AI SDK, Mastra, LangGraph.js, etc.)
OpenAI Agents SDK (Python, public preview)
Tasks as AI tools
ai.tool()
exposes tasks to Vercel AI SDK
activity_as_tool
exposes activities to OpenAI Agents SDK
Real-time streaming
Realtime Streams (to frontend and backend)
No dedicated streaming primitive
Frontend hooks
useRealtimeRun, useRealtimeStream, useWaitToken, useInputStreamSend
No frontend SDK
Human-in-the-loop
Waitpoints (pause for approval, webhooks, events)
Signals (external data into workflows)
Bidirectional communication
Input streams (typed data into running tasks from backend or frontend)
Signal/Query/Update
Max execution time
No limit
No limit
Multi-language agents
TypeScript only
Go, Java, Python, TypeScript, .NET, PHP
Temporal's AI story is strongest in Python, where the OpenAI Agents SDK wraps agent interactions as durable workflow steps with
activity_as_tool
, and Signal/Query/Update lets external systems push data into running agent workflows or query their state. If your AI agents are in Python or span multiple languages, Temporal is the natural fit. Trigger.dev takes a TypeScript-native approach: any AI framework (AI SDK, Mastra, LangGraph.js) works without wrappers, Realtime Streams push tokens to your frontend and backend, and Waitpoints pause tasks indefinitely for human approval or external events, and
input streams
let you send typed data into running tasks from your backend or frontend (cancel signals, approvals, or any structured payload).
What infrastructure do you need to manage?
Temporal gives you full control over your worker infrastructure, even on Cloud. Trigger.dev runs your code on managed compute with nothing to provision.
Feature
Trigger.dev
Temporal
Managed option
Trigger.dev Cloud (fully managed)
Temporal Cloud (server managed, workers are yours)
Self-hosted minimum
Docker Compose
Database + Elasticsearch + Server + Workers
Workers to deploy
None
At least one per task queue
Compute isolation
Each run gets its own container with configurable CPU/RAM
Activities share worker process resources
Time to production
~5 minutes
Days to weeks (self-hosted) or hours (Cloud)
License
Apache 2.0
MIT (server)
Temporal's architecture separates the server (orchestration) from workers (your code), giving you full control over where and how your code runs. Teams with strict compliance, data residency, or custom runtime needs require this level of control. Temporal Cloud manages the server side; you manage workers. Trigger.dev takes a different approach: write your task, run
npx trigger.dev@latest deploy
, and your code runs on managed compute with nothing to provision or scale. Each run gets its own container with a configurable machine preset, so a memory spike in one task can't affect others. Temporal workers share resources across activities on the same task queue, isolation requires dedicating separate task queues and worker pools. Both offer self-hosting: Trigger.dev via Docker Compose or Kubernetes (Apache 2.0), Temporal via its MIT-licensed server. Temporal Nexus connects workflows across namespace and region boundaries with typed service contracts, used by Netflix for cross-team orchestration. Trigger.dev has no equivalent.
How does pricing compare at scale?
Temporal bills per action across every workflow event. Trigger.dev bills per compute-second plus a per-run fee. The models favor different workload shapes.
Feature
Trigger.dev
Temporal
Pricing model
Compute-seconds + per-run fee
Per-action (every timer, signal, activity is billable)
Free tier
Free plan with compute credit included
Trial credits included
Self-hosted cost
Free (Apache 2.0) + your infra
Free (MIT) + significant infra
Essentials
—
Essentials tier with bundled actions
Business
—
Business tier with more bundled actions
Temporal's per-action model charges for every timer, signal, and activity across a workflow's lifecycle. A workflow with 5 activities may consume 15-20 actions. Trigger.dev's compute-second model charges for actual execution time regardless of internal operations. Temporal's model favors many short workflows with few steps. Trigger.dev's model favors longer-running tasks like AI summarization. Note that Temporal Cloud pricing covers orchestration only, so you pay separately for the compute to run your workers. Self-hosting either platform eliminates cloud fees entirely.
How do self-hosting and licensing compare?
Trigger.dev licenses its entire platform under Apache 2.0, while Temporal uses an MIT license for its server.
Feature
Trigger.dev
Temporal
License
Apache 2.0
MIT (server)
Minimum setup
Docker Compose
Database + Elasticsearch + Server + Workers
Production complexity
Docker Compose or Kubernetes
Database cluster + Elasticsearch + multiple services
Managed alternative
Trigger.dev Cloud
Temporal Cloud (paid tiers)
This server runs the exact full-featured codebase that powers Temporal Cloud, letting teams with dedicated platform engineering run it at massive scale. The setup involves a database cluster (PostgreSQL or Cassandra), Elasticsearch, and multiple server services. Trigger.dev self-hosts with Docker Compose for small deployments or Kubernetes for production, with the entire platform under Apache 2.0. Your choice between them comes down to how much operational surface area your team wants to manage.
Code comparison
Normal TypeScript vs deterministic workflows
Trigger.dev (1 file)
import
{
task
}
from
"@trigger.dev/sdk"
;
export
const
myTask
=
task
(
{
id
:
"my-task"
,
run
:
async
(
payload
:
{
url
:
string
}
)
=>
{
const
now
=
Date
.
now
(
)
;
// fine
const
id
=
crypto
.
randomUUID
(
)
;
// fine
const
data
=
await
fetch
(
payload
.
url
)
;
// fine
return
{
now
,
id
,
data
:
await
data
.
json
(
)
}
;
}
,
}
)
;
Temporal (2 files)
// workflow.ts
import
{
proxyActivities
}
from
'@temporalio/workflow'
;
import
type
*
as
activities
from
'./activities'
;
const
{
fetchData
}
=
proxyActivities
<
typeof
activities
>
(
{
startToCloseTimeout
:
'5 minutes'
,
}
)
;
export
async
function
myWorkflow
(
url
:
string
)
{
const
data
=
await
fetchData
(
url
)
;
return
{
data
}
;
}
// activities.ts
export
async
function
fetchData
(
url
:
string
)
{
const
response
=
await
fetch
(
url
)
;
const
now
=
Date
.
now
(
)
;
const
id
=
crypto
.
randomUUID
(
)
;
return
{
now
,
id
,
data
:
await
response
.
json
(
)
}
;
}
Normal TypeScript vs deterministic workflows
Trigger.dev (1 file)
Temporal (2 files)
import
{
task
}
from
"@trigger.dev/sdk"
;
export
const
myTask
=
task
(
{
id
:
"my-task"
,
run
:
async
(
payload
:
{
url
:
string
}
)
=>
{
const
now
=
Date
.
now
(
)
;
// fine
const
id
=
crypto
.
randomUUID
(
)
;
// fine
const
data
=
await
fetch
(
payload
.
url
)
;
// fine
return
{
now
,
id
,
data
:
await
data
.
json
(
)
}
;
}
,
}
)
;
AI document summarizer
Trigger.dev (1 file)
import
{
task
}
from
"@trigger.dev/sdk"
;
import
{
generateText
}
from
"ai"
;
import
{
anthropic
}
from
"@ai-sdk/anthropic"
;
export
const
summarizeDoc
=
task
(
{
id
:
"summarize-doc"
,
run
:
async
(
payload
:
{
documentUrl
:
string
}
)
=>
{
const
doc
=
await
fetch
(
payload
.
documentUrl
)
.
then
(
r
=>

[SCRAPER NOTE: This page was truncated by the scraper due to length. Content continues on the live page.]

---

## Trigger.dev vs BullMQ | Trigger.dev

**URL:** https://trigger.dev/vs/bullmq

Trigger.dev vs BullMQ | Trigger.dev
Updated
March 2026
Trigger.dev vs BullMQ
Every production app needs background jobs. BullMQ is the most popular way to run them in Node.js: 14M+ monthly downloads, MIT-licensed, and backed by Redis for raw throughput. Trigger.dev is a managed compute platform where those same jobs get durability, observability, and auto-scaling with nothing to provision. Choose BullMQ for lightweight queuing with full control over your stack. Choose Trigger.dev for TypeScript teams that want background jobs without managing Redis, workers, or scaling.
What is
Trigger.dev
?
Trigger.dev
is a managed compute platform for building AI agents and workflows in TypeScript. Your code runs as normal TypeScript with no determinism constraints and no execution timeout. It includes built-in retries, queues, scheduling, and OpenTelemetry observability with custom dashboards and a SQL-style query language. Tasks can stream data to your frontend in real-time, receive typed input while running, and pause indefinitely for human approval or external events. Thousands of engineering teams run production workloads on it, processing millions of runs.
What is
BullMQ
?
BullMQ
is a Redis-backed job queue library for Node.js with 14M+ monthly downloads, making it the most widely used background job solution in the JavaScript ecosystem. It supports delayed jobs, cron scheduling, job flows (parent-child dependencies), rate limiting, automatic retries with exponential backoff, priorities, sandboxed workers, and OpenTelemetry support (via official adapter). BullMQ is compatible with Redis, Valkey, DragonflyDB, ElastiCache (node-based clusters only, not serverless), and Upstash.
Feature deep-dive
How does developer experience and setup compare?
BullMQ gets you running in minutes with
npm install
plus a Redis connection. Trigger.dev gets you running with a CLI command and zero infrastructure to manage afterward.
Feature
Trigger.dev
BullMQ
What you install
npm package + CLI
npm package + Redis server
Infrastructure
Managed compute (Cloud) or self-hosted (Docker/K8s)
Redis + your Node.js worker processes
Time to first job
~5 minutes (CLI deploy)
~10 minutes (with existing Redis)
Worker management
Managed by platform
Your Node.js processes (PM2, Docker, K8s)
Scaling
Automatic
Add more worker processes
Dashboard
Dashboard with OpenTelemetry traces, logs, custom dashboards, TRQL query language, AI assistant, and alerting
BullBoard (community), Taskforce.sh (commercial), Bullstudio (community)
Child tasks
triggerAndWait
/
batchTriggerAndWait
Job flows via
FlowProducer
(unlimited nesting)
Delayed execution
delay option (duration string or date)
Delayed jobs (duration or timestamp)
Local development
Hot reload via CLI (internet required)
Fully offline with local Redis
Payload validation
schemaTask with Zod, ArkType, or TypeBox for runtime-validated payloads
No built-in validation
AI coding tools
MCP server (docs, metrics, write tasks, trigger, monitor, deploy), agent rules, skills, llms.txt
No equivalent
BullMQ's setup takes minutes: add the npm package, point it at Redis, and start processing jobs. The library gives you full control over workers, concurrency, and job lifecycle, and local development works fully offline. Trigger.dev takes a different approach:
npx trigger.dev@latest dev
starts local development,
npx trigger.dev@latest deploy
ships to production, and the platform handles workers, scaling, and monitoring. The tradeoff is control versus operational overhead.
Trigger.dev also ships an
MCP server
that lets AI editors deploy, trigger tasks, and monitor runs.
Agent rules
add code generation guidance for Claude Code, Cursor, Windsurf, VS Code, Zed, Gemini CLI, and Cline.
How do concurrency and rate limiting compare?
BullMQ provides per-worker concurrency, global rate limiting, and per-group controls (Pro). Trigger.dev provides per-queue and per-entity concurrency, debounce, idempotency keys, and dynamic overrides at trigger time.
Feature
Trigger.dev
BullMQ
Per-worker concurrency
Per-queue concurrency limits
Concurrency option per worker instance
Global rate limiting
Concurrency-based (no time-based rate limiting)
Per-second/minute/hour rate limiter
Per-entity controls
concurrencyKey
(e.g., per-user queues)
Groups with round-robin (Pro tier)
Dynamic overrides
Override queue and concurrency at trigger time
Set at queue/worker creation
Job priorities
Per-run priority at trigger time
Numeric priority per job (lower = higher)
Debounce
Built-in with leading/trailing modes and configurable delay
Part of deduplication (3 modes: simple, throttle, debounce)
Deduplication
Idempotency keys with configurable TTL
3 modes: simple, throttle, and debounce
Processing order
First-in-first-out (FIFO)
First-in-first-out (FIFO) and last-in-first-out (LIFO)
BullMQ's concurrency model is granular: set concurrency per worker instance, apply time-based rate limits (10 jobs per second), and use priorities to control processing order. BullMQ Pro extends this with group-level concurrency and round-robin processing across groups. Trigger.dev uses
concurrencyKey
to create per-entity queues (one concurrent job per user, per tenant, or per resource), and lets you override queue assignment at trigger time for patterns like different limits for free vs paid users. Trigger.dev also has built-in
debounce
(leading and trailing modes with configurable delay) and
idempotency keys
with TTL to prevent duplicate runs. Trigger.dev does not have time-based rate limiting, only concurrency-based controls.
How do reliability and failure recovery compare?
BullMQ reliability depends on your Redis persistence setup and retry configuration. Trigger.dev provides durable execution via checkpoint-resume, so tasks survive crashes and restarts automatically.
Feature
Trigger.dev
BullMQ
Failure recovery
Checkpoint-resume (durable execution)
Redis persistence + automatic retries
Data loss risk
None (checkpoints are durable)
Depends on Redis config (AOF: ~1s loss, RDB: minutes, none: all lost)
Retry mechanism
Built-in with configurable backoff
Built-in with configurable backoff
Long-running jobs
No timeout (hours, days, weeks)
No hard limit (stalled detection at 30s lock, configurable)
Delivery guarantee
At-least-once (with idempotency keys to prevent duplicates)
At-least-once (idempotency is your responsibility)
BullMQ's reliability comes from Redis persistence and its built-in retry mechanism. AOF with
appendfsync always
gives strong queue reliability at the cost of throughput. RDB snapshots are faster but can lose recent data. For teams already running Redis with proper persistence, BullMQ queues are reliable. Trigger.dev is a different category: durable execution. Checkpoint-resume snapshots your entire process state at wait points and restores it on recovery. Your code picks up exactly where it left off, not just the job getting retried from scratch.
How do AI agent capabilities compare?
BullMQ processes AI tasks as regular jobs with no new concepts to learn. Trigger.dev adds AI-specific features: real-time streaming, human-in-the-loop, and no execution timeout.
Feature
Trigger.dev
BullMQ
AI framework support
Any TS framework (AI SDK, Mastra, LangGraph.js, etc.). ai.tool() exposes tasks as LLM-callable tools
Any framework (it's a queue, not an AI platform)
Real-time streaming
Realtime Streams (SSE to frontend and backend)
Job progress events (numeric or custom object)
Human-in-the-loop
Waitpoints (pause indefinitely for approval)
No built-in equivalent
Bidirectional communication
Input streams (typed data into running tasks)
No built-in equivalent
Max execution time
No limit
No hard limit (tune stalledInterval for long jobs)
Stalled job detection
Heartbeat-based (managed by platform)
30s default lock, adjustable via lockDuration setting
Build customization
Build extensions install packages, SDKs, and system deps at build time (Prisma, FFmpeg, Playwright, Python, custom)
Your Dockerfile or package manager
BullMQ processes AI tasks the same way it processes any other job: no new concepts, no additional APIs. Long-running LLM calls work well with tuned
lockDuration
and
stalledInterval
settings. Job progress events provide status updates to callers. Trigger.dev adds features designed for AI workflows: Realtime Streams push tokens to your frontend over SSE,
input streams
send typed data into running tasks (cancel signals, approvals, user messages), and Waitpoints pause tasks indefinitely for human review. The managed compute model handles stalled detection automatically via heartbeats, so there's nothing to tune for long-running calls.
How does observability and debugging compare?
BullMQ provides an OpenTelemetry adapter and a community dashboard ecosystem. Trigger.dev includes built-in and custom dashboards, a SQL-style query language (TRQL), OpenTelemetry tracing, and structured logs for every run.
Feature
Trigger.dev
BullMQ
Dashboard
Built-in dashboard with run explorer, custom dashboards, and widgets (charts, tables, big numbers)
BullBoard (community), Taskforce.sh (commercial), Bullstudio
Query language
TRQL (SQL-style) queries against runs and metrics in ClickHouse, with AI assistant
No built-in query language
Tracing
OpenTelemetry traces per run with span-level detail
OpenTelemetry adapter (requires tracing backend)
Log capture
Structured logs attached to each run, viewable in dashboard
Application-level logging (stdout)
Error visibility
Stack traces, payloads, run history, and output diffs in dashboard
Error events via worker event handlers
Alerting
Built-in failure and success notifications (email, webhook)
Via monitoring stack (Grafana, Datadog, etc.)
Programmatic access
SDK and REST API for running queries from your code
Redis commands or dashboard API
Run tagging
Up to 10 tags per run, filterable in dashboard and SDK
No built-in tagging
BullMQ ships an OpenTelemetry adapter that integrates with your existing tracing infrastructure (Datadog, Grafana, Honeycomb). The dashboard ecosystem has grown: BullBoard for basic inspection, Taskforce.sh for commercial monitoring with SOC 2 compliance, and Bullstudio as a newer open-source option. Teams with an existing observability stack can instrument BullMQ thoroughly.
Trigger.dev includes observability out of the box: OpenTelemetry tracing with span-level detail, structured log capture, error visibility with full stack traces, and a run explorer that shows every run's payload, output, and timeline. Every project ships with a
built-in dashboard
, and you can build
custom dashboards
with charts, tables, and big number widgets.
TRQL
(a SQL-style query language backed by ClickHouse) lets you ask questions like "what are my most expensive runs?" or "what's the p95 duration for this task?" directly, or through the built-in AI assistant. You can also run queries from your code via the SDK or REST API to power internal tools or feed data to AI agents.
What infrastructure do you need to manage?
BullMQ is a library that runs in your Node.js process with Redis. Trigger.dev is a platform that runs your code on managed compute.
Feature
Trigger.dev
BullMQ
Managed option
Trigger.dev Cloud (fully managed)
Self-operated (Redis hosting via cloud providers)
Redis dependency
None
Redis, Valkey, DragonflyDB, ElastiCache, or Upstash
Worker deployment
npx trigger.dev@latest deploy
Your process manager (PM2, Docker, K8s)
Scaling
Automatic (managed compute)
Add more worker processes
Compute isolation
Each run gets its own container (configurable CPU/RAM)
Jobs share the worker process
Self-hosted option
Docker Compose or Kubernetes (Apache 2.0)
Always self-operated (MIT)
BullMQ's architecture is simple and well-understood: your Node.js process connects to Redis, enqueues jobs, and processes them. You control the entire stack, from Redis configuration (
maxmemory-policy: noeviction
is a hard requirement) to worker scaling and health monitoring. This is a strength for teams that want full control and already operate Redis in production. Trigger.dev provides managed compute: write a task, deploy it, and the platform handles scaling, isolation, and monitoring. Each run gets its own container with a configurable machine preset, so a memory spike in one task does not affect others. Both offer self-hosting: BullMQ is always self-operated (MIT), Trigger.dev runs on Docker Compose or Kubernetes (Apache 2.0).
How does the build and deploy pipeline compare?
Trigger.dev deploys with a single CLI command and manages build dependencies through config. BullMQ deploys as part of your existing Node.js application.
Feature
Trigger.dev
BullMQ
Build customization
Build extensions (Prisma, FFmpeg, Playwright, Python, custom)
Your Node.js toolchain and Docker image
Deploy integrations
GitHub auto-deploy, Vercel integration, CLI
Your CI/CD pipeline (GitHub Actions, etc.)
Environments
Production, Staging, Preview (per-branch), Development
Your environment setup (flexible, you control it)
System dependencies
FFmpeg, Puppeteer, Sharp, Python, etc. via extensions
Install via Dockerfile or package manager
BullMQ deploys as part of your Node.js application, so it uses whatever build and deploy pipeline you already have. If you are running Docker, you install system dependencies in your Dockerfile. Trigger.dev provides
build extensions
that add system-level dependencies (Prisma, FFmpeg, Playwright, Python) with a config line, plus custom extensions for anything not covered. The
GitHub integration
auto-deploys on every push, and
preview branches
create isolated environments per PR with their own API key, env vars, and schedules.
How do pricing and cost compare?
BullMQ is MIT-licensed and free. You pay for Redis hosting and your own compute. Trigger.dev bills per compute-second with a free tier included.
Feature
Trigger.dev
BullMQ
Infrastructure cost
Included in compute-second pricing
Redis hosting + worker compute (you manage)
Free tier
Free plan available
MIT (free forever) + your infrastructure costs
Pricing model
Compute-seconds + per-run fee
Your infrastructure costs (Redis + compute + monitoring tools)
Self-hosted cost
Free (Apache 2.0) + your infra
Free (MIT) + Redis + your compute
BullMQ's cost floor is genuinely low. The library is free, and a small Redis instance handles moderate workloads.
BullMQ Pro
adds groups, batches, and observables as a paid tier. As workloads grow, infrastructure costs include Redis scaling, worker compute, monitoring tools, and the engineering time to keep everything running.
Trigger.dev's pricing
is compute-seconds plus a per-run fee, with a free tier for getting started. Which is cheaper depends on workload shape: BullMQ's cost floor is low if you already run Redis, while Trigger.dev removes infrastructure and ops costs from the equation.
Code comparison
AI document summarizer
Trigger.dev
import
{
task
}
from
"@trigger.dev/sdk"
;
import
{
generateText
}
from
"ai"
;
import
{
anthropic
}
from
"@ai-sdk/anthropic"
;
export
const
summarizeDoc
=
task
(
{
id
:
"summarize-doc"
,
run
:
async
(
payload
:
{
documentUrl
:
string
}
)
=>
{
const
doc
=
await
fetch
(
payload
.
documentUrl
)
.
then
(
r
=>
r
.
text
(
)
)
;
const
{
text
}
=
await
generateText
(
{
model
:
anthropic
(
"claude-sonnet-4-20250514"
)
,
prompt
:
`
Summarize this document:\n\n
${
doc
}
`
,
}
)
;
return
{
summary
:
text
}
;
}
,
}
)
;
BullMQ
import
{
Queue
,
Worker
}
from
"bullmq"
;
import
{
generateText
}
from
"ai"
;
import
{
anthropic
}
from
"@ai-sdk/anthropic"
;
const
connection
=
{
host
:
"localhost"
,
port
:
6379
}
;
const
aiQueue
=
new
Queue
(
"ai-tasks"
,
{
connection
}
)
;
await
aiQueue
.
add
(
"summarize"
,
{
documentUrl
:
"https://example.com/doc.pdf"
,
}
)
;
const
worker
=
new
Worker
(
"ai-tasks"
,
async
(
job
)
=>
{
const
doc
=
await
fetch
(
job
.
data
.
documentUrl
)
.
then
(
r
=>
r
.
text
(
)
)
;
const
{
text
}
=
await
generateText
(
{
model
:
anthropic
(
"claude-sonnet-4-20250514"
)
,
prompt
:
`
Summarize this document:\n\n
${
doc
}
`
,
}
)
;
return
{
summary
:

[SCRAPER NOTE: This page was truncated by the scraper due to length. Content continues on the live page.]

---

## Changelog | Trigger.dev

**URL:** https://trigger.dev/changelog

Changelog | Trigger.dev
Changelog
All
Features
Versions
April 16
April 16
Input streams: send data into running tasks
Bidirectional task communication. Send typed data into running tasks from your backend or frontend, with four receiving patterns from suspending (frees compute) to non-blocking.
Eric Allam
Read changelog
April 13
April 13
Trigger.dev v
4.4.4
Task-level TTL defaults, 11 new MCP server tools, and major MCP improvements.
+
4
9
contributor
s
View release notes
March 10
March 10
Vercel integration
Connect your Vercel project to Trigger.dev and never run a manual deploy command again. Automatic deploys, env var sync, and atomic deployments
Oskar Otwinowski
Read changelog
March 10
March 10
Trigger.dev v
4.4.3
Error tracking dashboard, Supabase environment variable sync, and dev run auto-cancel on CLI exit.
4
contributor
s
View release notes
March 5
March 5
Query & Dashboards: analytics for your Trigger.dev data
Analyze your data using SQL for one-off queries or build custom dashboards with charts and tables.
Read changelog
March 4
March 4
Trigger.dev v
4.4.2
Input streams for bidirectional task communication, batch queue performance improvements, and security hardening.
2
contributor
s
View release notes
February 20
February 20
Trigger.dev v
4.4.1
OTEL metrics pipeline for task workers, MFA fix, and server improvements.
3
contributor
s
View release notes
February 19
February 19
Trigger.dev v
4.4.0
Metrics dashboards and query engine, Vercel integration, debounce maxDelay, and more.
+
7
12
contributor
s
View release notes
January 28
January 28
Trigger.dev agent skills for AI coding assistants
Install our official agent skills to teach any AI coding assistant best practices for writing tasks, agents, and workflows.
Dan Patel
Read changelog
January 24
January 24
Trigger.dev v
4.3.3
AI SDK 6 support, new limits page, better date and time filtering, improvements, bug fixes and server changes.
5
contributor
s
View release notes
January 22
January 22
AI SDK 6 support
Full compatibility with Vercel AI SDK 6 alongside existing 4 and 5 support.
Eric Allam
Read changelog
January 19
January 19
New limits page
New limits page to manage concurrency limits for your projects.
Read changelog
January 12
January 12
Improved date and time filtering in the dashboard
Redesigned date picker with visual calendar navigation, time precision controls, and quick preset options for faster run filtering.
James Ritchie
Read changelog
December 22
December 22
Debounced task runs
Consolidate multiple triggers into a single execution by debouncing task runs with a unique key and delay window.
Eric Allam
Read changelog
December 22
December 22
Batch trigger improvements
Support for larger payloads, streaming ingestion, and fair processing with per-environment concurrency limits.
Eric Allam
Read changelog
December 16
December 16
Adjacent task runs with ease
Tired of going back and forth between runs list and run details? Now you can easily navigate to the previous or next run directly from the run details page.
Oskar Otwinowski
Read changelog
December 12
December 12
Faster cold starts
Faster cold starts with zstd compression
We've enabled zstd compression by default for deployment images, improving cold start times when images need to be pulled to worker nodes.
Nick
Read changelog
December 10
December 10
Login with Google
You can now create an account or login to Trigger.dev with your Google account.
Read changelog
December 8
December 8
Deploy native builds
Deployments with native builds
Deploy your tasks with native builds using our own build infrastructure.
Saadi Myftija
Read changelog
December 5
December 5
Bun v1.3.3
Bun runtime upgraded to v1.3.3
We've upgraded the Bun runtime for deployments to v1.3.3, bringing improved performance and the latest features to your Bun-based tasks.
Nick
Read changelog
Load older updates
