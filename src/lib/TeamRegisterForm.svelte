<script lang="ts">
  type Team = "Blue" | "Red";
  let selectedTeam: Team = "Blue";

  const pickTeam = (team: Team) => {
    selectedTeam = team;
  };
</script>

<div>
  <label>Select a team ({selectedTeam})</label>
  <div class="flex flex-row">
    <button
      class={selectedTeam == "Blue"
        ? "focus:outline-none text-white rounded p-5 bg-blue-500 border-4 border-blue-600"
        : "focus:outline-none text-white rounded p-5 bg-blue-500 hover:bg-blue-600"}
      on:click={() => pickTeam("Blue")}
    >
      Blue
    </button>
    <button
      class={selectedTeam == "Red"
        ? "focus:outline-none text-white rounded p-5 bg-red-500 border-4 border-red-600"
        : "focus:outline-none text-white rounded p-5 bg-red-500 hover:bg-red-600"}
      on:click={() => pickTeam("Red")}
    >
      Red
    </button>
  </div>
</div>

<style>
</style>
