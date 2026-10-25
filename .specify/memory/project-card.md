# egovframe-portal-site-template: project context

## Role, scope, and public entry points

`README.md` describes a portal reference template providing notices/boards, users, authorization,
main-page content, FAQ/QnA, surveys, banners, and event-related template features.
`src/main/java/egovframework/com/` contains MVC/shared services, file handling, authentication
interception, and authorization components; `DATABASE/` holds schema/data assets.
Preserve routes, forms, session/authentication behavior, access checks, service and mapper contracts,
and database semantics. README explicitly marks site-introduction and civil-petition screens
as sample pages without implemented business behavior; do not invent completion requirements.

## Build and verification evidence

- `pom.xml` packages a WAR named `egovframe-template-portal`, inherits
  `org.egovframe.web:egovframe-web-config-parent:5.0.1`, and sets Java 17.
- `.github/workflows/maven.yml` targets `main` push/PR, uses JDK 17, and runs
  `mvn -B package --file pom.xml -Dmaven.test.skip=true`. This skips test compilation and
  execution. No workflow targeting `work` was observed; do not equate package success with
  successful tests, deployed authentication, or UI coverage.
- README Quickstart documents `mvn clean package`, then WAR deployment to a suitable server.
  Its IDE workflow requires schema/seed setup from `DATABASE/`, local configuration, and
  Run on Server. It lists JDK 17, Jakarta EE 9 / Servlet 5.0, and Spring 6.2.11;
  check actual build dependencies and target server before runtime maintenance.
- Runtime checks need a datasource, suitable schema/data, and configured servlet container.
  Maven Central/eGovFrame repository access is needed for dependencies. HSQL resources are
  present but have not been exercised. Use synthetic users/data and omit deployment secrets.

## Contribution and submission baseline

Actual parent: `eGovFramework/egovframe-portal-site-template`. No root AGENTS or contribution
guide was found in the file inventory. Fetch the actual upstream default branch and record its
SHA, preserving existing submission branches and open PRs. Prepare a missing `upstream-submit`
directly at that SHA. Later fixes use a separate upstream-based submission worktree, without
merging `work` or including tooling commits. Adoption artifacts stay on `work`; no PR is created.

## Exploration limits

No `.codegraph/` index was present. Context derives from targeted README, POM, CI, and source
path inspection. Application behavior, database setup, and tests were not exercised for adoption.


## Maintenance process

Follow [constitution.md](constitution.md) for the domain-card, assessment, planning, verification,
and submission gates. Commands are installed under `.omp/commands/`; read them as agent
instructions. No application build or test was run for tool adoption. Scaffold checks establish
tool installation only, not application correctness.
