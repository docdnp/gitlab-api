# gitlab-api

A small and self-contained shell script with convenience functions to communicate with the Gitlab API.

## Installation

Download the script, make it executable and place it within your PATH:

```shell
curl -Ls https://raw.githubusercontent.com/docdnp/gitlab-api/main/gitlab-api -o gitlab-api
chmod +x gitlab-api
```

## How to use

Ideally you start using:

```raw
gitlab-api init
```

Then you can call one of the commands described in gitlab-api's documentation:

```raw
Usage: gitlab-api <cmd> <args>
  query Gitlab API

 Docs:
   https://docs.gitlab.com/ee/api/rest

 Commands:
   allgroups                           return all groups
   allparents        <id> <chain>      return all parent ids starting by group <id> prepending <chain>
   allprojects                         return all projects
   api               <endpoint>        return API result for endpoint
   filter            <args>            return all matches where args build an arg1|arg2|...|argN
   forall            <cmd> <args>      call <cmd> with <args> for every input line (reference line in args with {})
   gron.filter       <args>            combine gron and filter <args>
   gron.grep         <args>            combine gron and grep <args>
   group.allrepos    <id>              return all repos under group with <id> (recursively)
   group.info        <id>              return group object of group with <id>
   group.repos       <id>              return all repos under group with <id>
   group.subgroups   <id>              return all subgroups under group with <id>
   help                                print this help text
   id                                  return digits after '=' in "path = id"
   init                                create configuration file ~/.glapi/glapi.conf
   project.info      <id>              return project object of project with <id>
   project.vars      <name>  <cifile>  return all CI variable of project <name> with <cifile:-.gitlab-ci.yml>
   rootgroup         <groupname>       return root group id of all projects in <groupname>
   search            <scope> <search>  return all items of <scope> (groups,projects) matching <search>
```
