<template>
  <div class="">
    <div class="main">
      <div class="inner">
        <div class="nested-inner">
          <div class="wrapper">
            <div class="content">
              <draggable
                v-model="myArray"
                @start="drag = true"
                @end="drag = false"
                class="drag"
              >
                <div v-for="element in myArray" :key="element.id">
                  <IconStars v-if="element === 1" />
                  <p contenteditable="true" v-if="element === 2">
                    All the text and elements in this popup should be editable
                    and draggable
                  </p>

                  <input
                    class="input"
                    type="text"
                    placeholder="E-mail"
                    v-if="element === 3"
                  />
                  <button
                    contenteditable="true"
                    class="button"
                    v-if="element === 4"
                  >
                    signup now
                  </button>
                </div>
              </draggable>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import IconStars from "@/components/IconStars.vue";
import draggable from "vuedraggable";

export default {
  components: { IconStars, draggable },
  data() {
    return {
      myArray: [1, 2, 3, 4],
    };
  },
};
</script>
