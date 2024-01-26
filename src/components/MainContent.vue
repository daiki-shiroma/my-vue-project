<template>
  <div class="main-content">
    <h2>Identify the company for interview purposes</h2>
    <p>Enter your company's basic information and core values, or provide a URL, to customize the interview to your organization's identity and culture.</p>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="companyName">Your Company Name</label>
        <input type="text" id="companyName" v-model="companyName" placeholder="">
      </div>
      <div class="form-group">
        <label for="companyValues">Your Company's Values</label>
        <textarea id="companyValues" v-model="companyValues" placeholder="or describe manually"></textarea>
        <button type="button" @click="fetchDetails">Fetch Details</button>
      </div>
      <div class="examples">
        <p>e.g.,</p>
        <ul>
          <li v-for="value in exampleValues" :key="value.title">{{ value.title }}: {{ value.description }}</li>
        </ul>
      </div>
      <button type="submit">Continue</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      companyName: '',
      companyValues: '',
      exampleValues: [
        // ... example values ...
      ]
    };
  },
  methods: {
    fetchDetails() {
      // Implement fetch details logic
    },
    submitForm() {
      // Implement form submission logic
    }
  }
};
</script>

<style scoped lang="scss">
.main-content {
  flex-grow: 1;
  padding: 20px;

  h2 {
    color: #333;
  }

  .form-group {
    margin-bottom: 20px;

    label {
      display: block;
    }

    input[type="text"],
    textarea {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
    }

    button {
      padding: 10px 20px;
      margin-top: 10px;
      background-color: #007bff;
      color: white;
      border: none;
    }
  }

  .examples {
    background: #f8f9fa;
    border-left: 5px solid #007bff;
    padding: 10px;

    ul {
      list-style: none;
      padding-left: 0;
    }
  }

  button[type="submit"] {
    background: #28a745;
    color: white;
    border: none;
    padding: 10px 20px;
    margin-top: 20px;
  }
}
</style>
