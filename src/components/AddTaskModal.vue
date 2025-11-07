<template>
    <div class="modal" id="addTaskModal">
        <div class="modal__overlay"></div>
        <div class="modal__content"> 
            <h2 class="modal__title">NEW NOTE</h2>
            <input type="text" class="modal__input" placeholder="Input your note..." name="" id="">
            <div class="modal__buttons">
                <button class="modal__button modal__button--cancel">
                    CANCEL
                </button>
                <button class="modal__button modal__button--apply">
                    APPLY
                </button>
            </div>
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped lang="scss">
    .modal {
        display: block;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: 1000;

        &__overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
        }

        &__content {
            position: relative;
            width: fit-content;
            border-radius: 16px;
            padding: 18px 30px;
            margin: 10% auto;
            background-color: var(--bg);
        }

        &__title {
            font-size: 24px;
            font-weight: 500;
            text-align: center;
        }

        &__input {
            width: 440px;
            margin-top: 25px;
            padding: 6px 16px;
            font-family: 'Kanit', 'Roboto', sans-serif;
            font-weight: 400;
            font-size: 16px;
            border-radius: 6px;
            border-width: 1px;
            border-color: var(--input);
            background-color: var(--bg);
            color: var(--text);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            &::placeholder { color: var(--input-text);}
            &:focus {
                outline: none;
                box-shadow: 0 0 0 3px var(--input-shadow);
            }
        }

        &__buttons {
            display: flex;
            justify-content: space-between;
            margin-top: 128px;
            gap: 50px;
        }

        &__button {
            font-family: 'Kanit', sans-serif;
            font-size: 18px;
            font-weight: 500;
            background-color: var(--bg);
            padding: 8px 22px;
            border-radius: 6px;
            border: 2px solid transparent;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            cursor: pointer;
            &--cancel {
                color: var(--button);
                border-color: var(--button);
                &:hover {
                    background-color: var(--button-focus-light);
                    box-shadow: 0 0 3px 0 var(--button);
                }
            }
            &--apply {
                background-color: var(--button);
                color: var(--button-text);
                &:hover {
                    background-color: var(--button-focus);
                    box-shadow: 0 0 3px 0 var(--button);
                }
            }
        }
    }
</style>
