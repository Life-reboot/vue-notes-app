<template>
  <div class="note-selectors">
    <note-selector v-for="note in notes" v-bind:note="note" v-bind:key="note.id" />
  </div>
</template>

<script>
import NoteSelector from "./NoteSelector";

export default {
  name: "note-selectors",
  components: {
    NoteSelector,
  },
  data: function() {
    return {
      notes: [
        { id: 1, body: "This is the first note", timestamp: Date.now() },
        { id: 2, body: "This is the second note", timestamp: Date.now() },
        { id: 3, body: "This is the third note", timestamp: Date.now() },
        { id: 4, body: "This is the fourth note", timestamp: Date.now() },
      ],
    };
  },
};
</script>