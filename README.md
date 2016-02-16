//this is currently a test

void CAI_BaseNPC::RunAI( void )
{
	g_AIRunTimer.Start();

	GatherConditions();

	TryRestoreHull();

	g_AIPrescheduleThinkTimer.Start();

	PrescheduleThink();

	g_AIPrescheduleThinkTimer.End();

	MaintainSchedule();

	PostscheduleThink();

	ClearTransientConditions();

	g_AIRunTimer.End();
}
