<script setup></script>

<template>
  <header>
    <div>
      <button :disabled="true">Add Member (0 Spots Left)</button>
    </div>
    <div>
      <h3>
        Smiley team
        <div>5</div>
      </h3>
    </div>
  </header>
  <div>
    <table>
      <thead>
        <tr>
          <th>Name</th>
          <th>Email</th>
          <th>Status</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Member 1</td>
          <td>member1@gmail.com</td>
          <td>
            <button>Active</button>
          </td>
        </tr>
        <tr>
          <td>Member 2</td>
          <td>member2@gmail.com</td>
          <td>
            <button>Active</button>
          </td>
        </tr>
        <tr>
          <td>Member 3</td>
          <td>member3@gmail.com</td>
          <td>
            <button>Active</button>
          </td>
        </tr>
      </tbody>
    </table>
    <p>There are no remaining team spots. Upgrade to add more.</p>
  </div>
  <footer>
    <h5>Smiley - 5 member Team</h5>
  </footer>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1.5rem;
}

header button {
  min-width: 180px;
}

header h3 {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin: 0;
}

header h3 div {
  background: #0d6efd;
  color: #fff;
  border-radius: 50%;
  width: 2.2rem;
  height: 2.2rem;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}

table {
  width: 100%;
  margin-bottom: 1rem;
}

th,
td {
  text-align: left;
  padding: 0.75rem;
  vertical-align: middle;
}

thead {
  background: #f8f9fa;
}

tbody tr:nth-child(even) {
  background: #f2f2f2;
}

button {
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 0.3rem;
  background: #0d6efd;
  color: #fff;
  cursor: pointer;
}

button:disabled {
  background: #adb5bd;
  cursor: not-allowed;
}

footer {
  margin-top: 2rem;
  text-align: center;
  color: #6c757d;
}
</style>
