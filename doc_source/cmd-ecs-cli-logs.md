# ecs\-cli logs<a name="cmd-ecs-cli-logs"></a>

Retrieves container logs from CloudWatch Logs\. Only valid for tasks that use the `awslogs` driver and have a log stream prefix specified\.

**Important**  
Some features described may only be available with the latest version of the Amazon ECS CLI\. To obtain the latest version, see [Installing the Amazon ECS CLI](ECS_CLI_installation.md)\.

## Syntax<a name="cmd-ecs-cli-logs-syntax"></a>

**ecs\-cli logs \-\-task\-id *task\_id* \[\-\-task\-def *task\_definition*\] \[\-\-follow\] \[\-\-filter\-pattern *search\_string*\] \[\-\-since *n\_minutes*\] \[\-\-start\-time *2006\-01\-02T15:04:05\+07:00*\] \[\-\-end\-time *2006\-01\-02T15:04:05\+07:00*\] \[\-\-timestamps\] \[\-\-help\]** 

## Options<a name="cmd-ecs-cli-logs-options"></a>


| Name | Description | 
| --- | --- | 
|  `--task-id task_id`  |  Prints the logs for this ECS task\. Type: String Required: Yes  | 
|  `--task-def task_definition`  |  Specifies the name or full Amazon Resource Name \(ARN\) of the ECS task definition associated with the task ID\. This is only needed if the task has been stopped\. Type: String Required: No  | 
|  `--follow`  |  Specifies if the logs should be streamed\. Required: No  | 
|  `--filter-pattern search_string`  |  Specifies the substring to search for within the logs\. Type: String Required: No  | 
|  `--since n`  |  Returns logs newer than a relative duration in minutes\. Can't be used with `--start-time`\. Type: Integer Required: No  | 
|  `--start-time timestamp`  |  Returns logs after a specific date \(format: RFC 3339\. Example: `2006-01-02T15:04:05+07:00`\)\. Cannot be used with `--since` flag\. Required: No  | 
|  `--end-time timestamp`  |  Returns logs before a specific date \(format: RFC 3339\. Example: `2006-01-02T15:04:05+07:00`\)\. Cannot be used with `--follow`\. Required: No  | 
|  `--timestamps`  |  Specifies if timestamps are shown on each line in the log output\. Required: No  | 
|  `--help, -h`  |  Shows the help text for the specified command\. Required: No  | 

## Examples<a name="cmd-ecs-cli-logs-examples"></a>

### Example<a name="cmd-ecs-cli-logs-example-1"></a>

This example prints the log for a task\.

```
ecs-cli logs --task-id task_id
```

The contents of the log is in the output if successful\.