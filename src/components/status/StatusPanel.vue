<template>
    <div>
        <button @click="showModal = true">Show Modal</button>
        <!-- use the modal component, pass in the prop -->
        <Modal v-if="showModal" @close="showModal = false">
            <WakatimePlugin/>
        </Modal>
    </div>
</template>

<script>
import WakatimePlugin from "./WakatimePlugin.vue";
import Modal from "../ui/Modal.vue";
export default {
  name: "StatusPanel",
  components: {
    WakatimePlugin,
    Modal
  },
  data() {
    showModal: false;
  },
  methods: {
    log(e) {
      console.log(e);
    }
  }
};
</script>