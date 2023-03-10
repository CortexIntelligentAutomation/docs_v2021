| Component                                         | Purpose                                                                                     | Required/Optional           | Server Role                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------|-----------------------------|--------------------------------------------|
| [Cortex Gateway][Gateway Guide]                   | {{< section "/architecture/components/purpose/cortex-gateway.md" >}}               | Required                    | Web Application Server                     |
| [Cortex Studio][Studio Guide]                     | {{< section "/architecture/components/purpose/cortex-studio.md" >}}                | Required                    | Web Application Server                     |
| [Cortex Flow Debugger Service][]                  | {{< section "/architecture/components/purpose/cortex-flow-debugger-service.md" >}} | Required                    | Web Application Server                     |
| [Cortex API Gateway Service][]                    | {{< section "/architecture/components/purpose/cortex-api-gateway-service.md" >}}   | Required                    | Application Server                         |
| [Cortex Execution Service][]                      | {{< section "/architecture/components/purpose/cortex-execution-service.md" >}}     | Required                    | Application Server                         |
| [Cortex Package Service][]                        | {{< section "/architecture/components/purpose/cortex-package-service.md" >}}       | Required                    | Application Server                         |
| [Cortex Provisioning Service][]                   | {{< section "/architecture/components/purpose/cortex-provisioning-service.md" >}}  | Required                    | Application Server                         |
| Cortex Block Packages                             | {{< section "/architecture/components/purpose/cortex-block-packages.md" >}}        | Required                    | Web Application Server, Application Server |
| Cortex Gateway Databases                          | {{< section "/architecture/components/purpose/cortex-gateway-databases.md" >}}     | Required<br />(End of life) | Web Application Server                     |
| [SQL Server Express][] or [SQL Server Standard][] | {{< section "/architecture/components/purpose/ms-sql-server.md" >}}                | Required<br />(End of life) | Web Application Server                     |
| [Microsoft Service Fabric][]                      | {{< section "/architecture/components/purpose/ms-service-fabric.md" >}}            | Required                    | Application Server                         |
| [Microsoft Service Fabric Explorer][]             | {{< section "/architecture/components/purpose/ms-service-fabric-explorer.md" >}}   | Required                    | Application Server                         |
| [Particular NServiceBus][]                        | {{< section "/architecture/components/purpose/particular-nservicebus.md" >}}       | Required                    | Application Server                         |
| [Pivotal RabbitMQ][]                              | {{< section "/architecture/components/purpose/pivotal-rabbitmq.md" >}}             | Required                    | Application Server                         |
| [Erlang OTP][]                                    | {{< section "/architecture/components/purpose/erlang-otp.md" >}}                   | Required                    | Application Server                         |
| [gobetween][]                                     | {{< section "/architecture/components/purpose/gobetween.md" >}}                    | Required                    | Load Balancer                              |
| [NSSM][]                                          | {{< section "/architecture/components/purpose/nssm.md" >}}                         | Required                    | Load Balancer                              |

[Cortex API Gateway Service]: {{< url "Cortex.Guides.ApiGatewayService.MainDoc" >}}
[Cortex Flow Debugger Service]: {{< url "Cortex.Guides.FlowDebuggerService.MainDoc" >}}
[Cortex Execution Service]: {{< url "Cortex.Guides.ExecutionService.MainDoc" >}}
[Cortex Package Service]: {{< url "Cortex.Guides.PackageService.MainDoc" >}}
[Cortex Provisioning Service]: {{< url "Cortex.Guides.ProvisioningService.MainDoc" >}}
[Gateway Guide]: {{< url "Cortex.Guides.Gateway.MainDoc" >}}
[Studio Guide]: {{< url "Cortex.Guides.Studio.MainDoc" >}}
[SQL Server Express]: {{< url "MSDownload.SqlServerExpress.2016" >}}
[SQL Server Standard]: {{< url "MSEval.SQLServer.2019" >}}
[Microsoft Service Fabric]: {{< url "MSDocs.ServiceFabric.MainDoc" >}}
[Microsoft Service Fabric Explorer]: {{< url "MSDocs.ServiceFabric.Explorer" >}}
[Particular NServiceBus]: {{< url "Particular.NServiceBus.MainDoc" >}}
[Pivotal RabbitMQ]: {{< url "RabbitMQ.MainDoc" >}}
[Erlang OTP]: {{< url "ErlangOTP.MainDoc" >}}
[gobetween]: {{< url "GoBetween.MainDoc" >}}
[NSSM]: {{< url "NSSM.MainDoc" >}}