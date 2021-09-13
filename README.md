<!---
Button Style 
--->

:root{
    --grad1: #03a9f4;
    --grad2: #f441a5;
    --grad3: #ffeb3b;
    --grad4: #03a9f4;
}

selector a{
	background: linear-gradient(90deg, var(--grad1), var(--grad2), var(--grad3), var(--grad4));
	background-size: 400%;
	z-index: 1;
	position: relative;
}
selector a:hover{
	animation: animate 8s linear infinite;
}
@keyframes animate {
	0%{
		background-position: 0%;
	}
	100%{
		background-position: 400%;
	}
}

<!---------------------------------------------------->
/*css for glowing background*/
selector a:before{
	content: '';
	position: absolute;
	top: -5px;
	left: -5px;
	right: -5px;
	bottom: -5px;
	z-index: 0;
	background: linear-gradient(90deg, var(--grad1), var(--grad2), var(--grad3), var(--grad4));
	background-size: 400%;
	border-radius: 40px;
	opacity: 0;
	transition: 0.5s;

}
selector a:hover:before{
	filter: blur(20px);
	opacity: .6;
	animation: animate 8s linear infinite;
}
