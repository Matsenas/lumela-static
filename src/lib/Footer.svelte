<div id="footer">
    <p>
        hey@lumela.ee
    </p>
</div>


<style lang="scss">
    #footer {
        position: fixed;
        bottom: 40px;
        width: 100%;
        will-change: transform;
        transition: transform 500ms ease-out;
        -webkit-animation: fadein 3s; /* Safari, Chrome and Opera > 12.1 */
        -moz-animation: fadein 3s; /* Firefox < 16 */
        -ms-animation: fadein 3s; /* Internet Explorer */
        -o-animation: fadein 3s; /* Opera < 12.1 */
        animation: fadein 3s;
        p {
            margin: 0;
        }
    }

    #footer:hover {
        transform: scale(1.05);
    }
</style>