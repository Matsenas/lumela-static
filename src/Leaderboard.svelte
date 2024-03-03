<script>
import { onMount } from 'svelte';
  
/**
** @type {any[]}
*/
let publishers = [];

onMount(async () => {
  const response = await fetch('https://eu-central-1.aws.data.mongodb-api.com/app/firn-prototype-app-gzaxx/endpoint/top/publishers');
  if (response.ok) {
    publishers = await response.json();
  } else {
    console.error('Failed to fetch publishers:', response.statusText);
  }
});
</script>
  
<style>
/* Add some basic styling for the leaderboard */
.leaderboard {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.publisher {
  display: flex;
  justify-content: space-between;
  width:  50%;
  padding:  10px;
  border-bottom:  1px solid #f0f0f0;
}
.publisher:last-child {
  border-bottom: none;
}

.name {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.balance {
  font-size: 14px;
  font-weight: 700;
}
</style>
  
<div class="leaderboard">
  <h1>Top Publishers</h1>
  {#each publishers as publisher (publisher._id)}
    <div class="publisher">
      <div class="name">
        <div>
          <strong>{publisher.baseDomain}</strong>
          <span>{publisher.name ? `(${publisher.name})` : ''}</span>
          <span style="font-style: italic;">{publisher.verified ? '✅' : ''}</span>
        </div>
      </div>
      <div>
        <span class="balance">{publisher.balance/100}€</span>
      </div>
    </div>
  {/each}
</div>