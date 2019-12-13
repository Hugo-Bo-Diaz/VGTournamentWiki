<html>
<h2>The project</h2>
	<p>
	This game was done as a part of the AI subject for the the UPC's Bachelor's degree, with some movement scripts given by the teachers, as well as the SimpleAssets pack for the art
	</p>
	<p>
	The game was done in the span of 3 months between October and December, this was the order of execution:
		<ol>
			<li>The environment, making sure that the agents could more appropiately</li>
			<li>Designed and implemented the Behaviour Trees for the different agents</li>
			<li>Gameplay and balancing</li>
		</ol>
	</p>
<h2>The AI</h2>
	<p>
	The Behaviour Trees (BTs) were done with NodeCanvas and they are the following
	</p>
	<h3>Participants:</h3>
		<h4>FSM:</h4>
			<img src="images/FSM-BT/ParticipantFSM.PNG" alt="Participant FSM">
			<p>
			They will wander around until called and will reset to this when any behaviour ends.
			</p>
		<h4>Behaviour trees:</h4>
			<p><b>Leaving BT:</b></p>
				<img src="images/FSM-BT/ParticipantLeaveBT.PNG" alt="Participant Leave BT">
				<p>
				This is a very simple BT, this will just take the participant to the entrance and delete him.
				</p>
			<p><b>Play Match BT:</b></p>
				<img src="images/FSM-BT/ParticipantPlayBT.PNG" alt="Participant Play Match BT">
				<p>
				This will take the player to the setup, then make him wait for the other player to be ready. After that he will go tell the TO the result if he won, then go home and go back to wandering.
				</p>
			<p><b>Wander BT</b></p>
				<img src="images/FSM-BT/ParticipantWanderBT.PNG" alt="Participant Wander BT">	
				<p>
				This will make him wander around and sometimes grab a drink.
				</p>
	<h3>Organizers:</h3>
		<h4>FSM:</h4>
			<img src="images/FSM-BT/TOFSM.PNG" alt="Organizer FSM">
			<p>
			This will just make him wander until he has to call a match.
			</p>
		<h4>Behaviour trees:</h4>
			<p><b>Call players to match BT:</b></p>
				<img src="images/FSM-BT/TOCallPlayerBT.PNG" alt="Organizer call match BT">
				<p>
				This BT will take the TO to the different players he was assigned, calling them 1 by 1 and telling them the setup they are supposed to play in, after that he will go to his homeplace to wander on his area
				</p>
	<h3>Technicians</h3>
		<h4>Behaviour Trees:</h4>
			<p>
			Contrary to the Organizers and Participants the Technicians are simple enough to be able to work on a BT, here is the main BT that he uses:
			</p>
			<img src="images/FSM-BT/TechnicianBT.PNG" alt="Technician BT">
			<p>
			He'll wander until he has a task assigned, then he will do it, after which the BT will restart and set him to wait again for a task
			</p>
</html>