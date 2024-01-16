<div id="coming-soon" class="unselectable">
    <span>coming</span>
    <span style="align-self: flex-end;">soon</span>
</div>

<style lang="scss">
#coming-soon {
    z-index: -2;
    position: fixed;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    font-size: 250px;
    font-style: italic;
    font-weight: 900;
    opacity: 10%;
    span {
        background: linear-gradient(
            60deg,
            #9A9090 0%,
            #9A909020 100%
        );
        -webkit-background-clip: text;
        background-clip: text;
        background-size: 500% auto;
        animation: 
        fadein 5s
        textShine 5s ease-in-out infinite alternate,
        bounce 5s ease-in-out infinite alternate;
        
        -webkit-animation: 
        fadein 5s,
        textShine 5s ease-in-out infinite alternate,
        bounce 5s ease-in-out infinite alternate; /* Safari, Chrome and Opera > 12.1 */
        
        -moz-animation: 
        fadein 5s,
        textShine 5s ease-in-out infinite alternate,
        bounce 5s ease-in-out infinite alternate; /* Firefox < 16 */
        
        -o-animation: 
        fadein 5s,
        textShine 5s ease-in-out infinite alternate,
        bounce 5s ease-in-out infinite alternate; /* Opera < 12.1 */

        -ms-animation: fadein 2s; /* Internet Explorer */
    
    }
}
  </style>