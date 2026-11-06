# Finance AI Backend V4 - Microsoft Agent Framework
1. Deploy existing core/api/accounting schemas, then orchestrator.sql.
2. Configure Microsoft Entra values, FinanceDb, AgentFramework AzureOpenAIEndpoint and Model via secure configuration.
3. In Azure production, use managed identity/RBAC for SQL and Azure OpenAI where available.
4. POST /v1/agents/chat routes the request, loads grounded SQL context, invokes Microsoft Agent Framework AIAgent using Azure OpenAI Responses, and returns FinanceAgentResult.
5. The agent has no financial side-effect tools. Posting/payment/filing/approval stays behind deterministic controls and human approval.
